# [Linux] Bash readonly brug: Gør variabler uforanderlige

## Overview
`readonly`-kommandoen i Bash bruges til at erklære variabler som uforanderlige. Når en variabel er markeret som readonly, kan dens værdi ikke ændres eller slettes i den nuværende shell-session. Dette er nyttigt for at beskytte vigtige værdier mod utilsigtede ændringer.

## Usage
Den grundlæggende syntaks for `readonly`-kommandoen er:

```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: Vis alle readonly variabler i den nuværende shell-session.

## Common Examples

### Eksempel 1: Opret en readonly variabel
```bash
readonly MY_VAR="Hello, World!"
```

### Eksempel 2: Forsøg på at ændre en readonly variabel
```bash
MY_VAR="New Value"  # Dette vil give en fejl, da MY_VAR er readonly
```

### Eksempel 3: Vis alle readonly variabler
```bash
readonly -p
```

## Tips
- Brug `readonly` til at beskytte konfigurationsvariabler, så de ikke utilsigtet ændres.
- Husk, at `readonly` kun gælder for den nuværende shell-session; hvis du åbner en ny session, skal du erklære variablerne igen.
- Overvej at bruge `readonly` i scripts for at sikre, at vigtige værdier forbliver konstante under kørslen.