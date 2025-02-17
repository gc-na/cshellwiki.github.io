# [Linux] Bash if brug: Kontroller betingelser

## Overview
`if` kommandoen i Bash bruges til at evaluere betingelser og udføre kommandoer baseret på resultatet af disse betingelser. Det er en grundlæggende del af kontrolstrukturen i scripts, der gør det muligt at træffe beslutninger.

## Usage
Den grundlæggende syntaks for `if` kommandoen er som følger:

```bash
if [ betingelse ]; then
    kommandoer
fi
```

## Common Options
- `-e`: Kontrollerer om en fil eksisterer.
- `-d`: Kontrollerer om en fil er en mappe.
- `-f`: Kontrollerer om en fil er en almindelig fil.
- `-z`: Kontrollerer om en streng er tom.
- `-eq`: Sammenligner to tal for lighed.

## Common Examples

### Eksempel 1: Tjek om en fil eksisterer
```bash
if [ -e "minfil.txt" ]; then
    echo "Filen eksisterer."
else
    echo "Filen findes ikke."
fi
```

### Eksempel 2: Tjek om en mappe eksisterer
```bash
if [ -d "minmappe" ]; then
    echo "Mappen eksisterer."
else
    echo "Mappen findes ikke."
fi
```

### Eksempel 3: Tjek om en variabel er tom
```bash
my_var=""
if [ -z "$my_var" ]; then
    echo "Variablen er tom."
else
    echo "Variablen har en værdi."
fi
```

### Eksempel 4: Sammenligning af tal
```bash
num1=10
num2=20
if [ $num1 -lt $num2 ]; then
    echo "$num1 er mindre end $num2."
else
    echo "$num1 er ikke mindre end $num2."
fi
```

## Tips
- Husk at inkludere mellemrum omkring `[` og `]` i betingelsen.
- Brug `elif` til at tilføje flere betingelser.
- Indsæt altid `fi` for at afslutte `if` blokken.
- Test dine betingelser i terminalen for at sikre, at de fungerer som forventet, før du bruger dem i scripts.