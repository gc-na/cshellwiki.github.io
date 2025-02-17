# [Linux] Bash cp brug: Kopier filer og mapper

## Overview
`cp`-kommandoen bruges til at kopiere filer og mapper fra et sted til et andet i Linux. Den er en grundlæggende del af filhåndtering i Bash og gør det muligt for brugere at oprette kopier af data hurtigt og effektivt.

## Usage
Den grundlæggende syntaks for `cp`-kommandoen er som følger:

```bash
cp [options] [source] [destination]
```

## Common Options
Her er nogle almindelige muligheder for `cp`-kommandoen:

- `-r`: Kopierer mapper rekursivt, hvilket betyder, at alle filer og undermapper også kopieres.
- `-i`: Spørger brugeren om bekræftelse, før der overskrives en eksisterende fil.
- `-u`: Kopierer kun filer, hvis kilden er nyere end destinationen eller hvis destinationen ikke eksisterer.
- `-v`: Viser detaljerede oplysninger om, hvad der bliver kopieret.

## Common Examples
Her er nogle praktiske eksempler på brug af `cp`-kommandoen:

1. Kopiere en enkelt fil til en ny placering:
   ```bash
   cp fil.txt /sti/til/destination/
   ```

2. Kopiere en mappe og dens indhold rekursivt:
   ```bash
   cp -r mappe /sti/til/destination/
   ```

3. Kopiere en fil og spørge om bekræftelse, hvis filen allerede findes:
   ```bash
   cp -i fil.txt /sti/til/destination/
   ```

4. Kopiere en fil og vise, hvad der bliver kopieret:
   ```bash
   cp -v fil.txt /sti/til/destination/
   ```

5. Opdatere en fil kun, hvis kilden er nyere:
   ```bash
   cp -u fil.txt /sti/til/destination/
   ```

## Tips
- Brug `-i`-muligheden for at undgå utilsigtet overskrivning af filer.
- Når du kopierer store mapper, kan `-v` være nyttig for at følge med i, hvad der bliver kopieret.
- Overvej at bruge `rsync` til mere komplekse kopieringsopgaver, især over netværk, da det tilbyder flere funktioner og bedre kontrol.