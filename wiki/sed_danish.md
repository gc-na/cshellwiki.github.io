# [Linux] Bash sed brug: Rediger tekststrømme

## Oversigt
`sed` (stream editor) er et kraftfuldt værktøj i Bash, der bruges til at manipulere og redigere tekststrømme. Det kan udføre en række operationer, såsom at søge, erstatte, indsætte og slette tekst.

## Brug
Den grundlæggende syntaks for `sed` er som følger:

```bash
sed [muligheder] [argumenter]
```

## Almindelige muligheder
- `-e`: Angiver en kommando, der skal udføres.
- `-i`: Ændrer filen in-place (direkte i filen).
- `-n`: Undertrykker automatisk udskrivning af linjer (kun udskriv linjer, der matches).
- `s`: Bruges til at erstatte tekst (substitution).

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `sed` kan bruges:

### Erstatte tekst
Erstatte "kat" med "hund" i en tekstfil:

```bash
sed 's/kat/hund/' fil.txt
```

### Erstatte tekst in-place
Erstatte "kat" med "hund" direkte i filen:

```bash
sed -i 's/kat/hund/' fil.txt
```

### Slette linjer
Slette linjer, der indeholder ordet "kat":

```bash
sed '/kat/d' fil.txt
```

### Indsætte linjer
Indsætte en linje før linje 2:

```bash
sed '2i Dette er en ny linje' fil.txt
```

### Udskrive specifikke linjer
Udskrive kun linje 3 fra en fil:

```bash
sed -n '3p' fil.txt
```

## Tips
- Brug `-i.bak` for at lave en sikkerhedskopi af filen, før du ændrer den.
- Test dine `sed`-kommandoer uden `-i` først for at sikre, at de fungerer som forventet.
- Kombiner flere `sed`-kommandoer med `-e` for at udføre flere operationer i én kommando.