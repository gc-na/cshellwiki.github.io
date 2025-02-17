# [Linux] Bash sort brug: Sorterer linjer i tekstfiler

## Overview
`sort`-kommandoen bruges til at sortere linjer i tekstfiler eller inputstrømme. Den kan sortere data alfabetisk, numerisk eller efter specifikke kriterier, hvilket gør den til et nyttigt værktøj til at organisere information.

## Usage
Den grundlæggende syntaks for `sort`-kommandoen er som følger:

```bash
sort [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `sort`-kommandoen:

- `-n`: Sorter numerisk.
- `-r`: Sorter i omvendt rækkefølge.
- `-k`: Angiv en specifik kolonne at sortere efter.
- `-u`: Fjern dubletter fra output.
- `-o`: Angiv en fil til at gemme det sorterede output.

## Common Examples
Her er nogle praktiske eksempler på brugen af `sort`:

1. Sorter en tekstfil alfabetisk:
   ```bash
   sort fil.txt
   ```

2. Sorter en tekstfil numerisk:
   ```bash
   sort -n tal.txt
   ```

3. Sorter i omvendt rækkefølge:
   ```bash
   sort -r fil.txt
   ```

4. Sorter efter en specifik kolonne (f.eks. den anden kolonne):
   ```bash
   sort -k2 fil.txt
   ```

5. Fjern dubletter fra output:
   ```bash
   sort -u fil.txt
   ```

6. Gem det sorterede output i en ny fil:
   ```bash
   sort -o sorterede_fil.txt fil.txt
   ```

## Tips
- Brug `-n` for at sikre, at numeriske værdier sorteres korrekt.
- Kombiner flere muligheder for at opnå det ønskede resultat, f.eks. `sort -n -r` for at sortere numerisk i omvendt rækkefølge.
- Hvis du arbejder med store filer, kan det være en god idé at bruge `-o` for at gemme output direkte til en fil og undgå at fylde terminalen.