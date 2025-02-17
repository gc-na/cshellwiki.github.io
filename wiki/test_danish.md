# [Linux] Bash test brug: Evaluering af betingelser

## Oversigt
`test`-kommandoen bruges i Bash til at evaluere betingelser og returnere en exit-status baseret på resultatet. Det er ofte anvendt i scripts til at kontrollere, om filer eksisterer, om variabler er tomme, eller til at sammenligne værdier.

## Brug
Den grundlæggende syntaks for `test`-kommandoen er:

```bash
test [options] [arguments]
```

## Almindelige muligheder
- `-e`: Tjekker om en fil eksisterer.
- `-d`: Tjekker om en sti er en mappe.
- `-f`: Tjekker om en sti er en fil.
- `-z`: Tjekker om en streng er tom.
- `-n`: Tjekker om en streng ikke er tom.
- `=`: Sammenligner to strenge for lighed.
- `-lt`, `-le`, `-gt`, `-ge`, `-eq`, `-ne`: Sammenligner numeriske værdier.

## Almindelige eksempler

### Tjek om en fil eksisterer
```bash
if test -e fil.txt; then
    echo "Filen eksisterer."
else
    echo "Filen findes ikke."
fi
```

### Tjek om en variabel er tom
```bash
variabel=""
if test -z "$variabel"; then
    echo "Variablen er tom."
else
    echo "Variablen har en værdi."
fi
```

### Sammenlign to tal
```bash
a=5
b=10
if test $a -lt $b; then
    echo "$a er mindre end $b."
fi
```

### Tjek om en sti er en mappe
```bash
if test -d /path/to/directory; then
    echo "Det er en mappe."
else
    echo "Det er ikke en mappe."
fi
```

## Tips
- Brug `[` i stedet for `test` for at gøre syntaksen mere læsbar: `[` er en synonym for `test`.
- Husk at afslutte `[` med `]`, når du bruger det.
- For mere komplekse betingelser kan du kombinere flere tests med `&&` (og) og `||` (eller).
- Overvej at bruge `[[` i stedet for `[` for at få mere avancerede funktioner som mønster-matching.