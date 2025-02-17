# [Linux] Bash source brug: Kør et script i den nuværende shell

## Overview
`source`-kommandoen bruges til at køre et shell-script i den nuværende shell-session. Dette gør det muligt for scriptet at ændre miljøvariabler og funktioner i den aktive shell, i modsætning til at køre det i en ny subshell.

## Usage
Den grundlæggende syntaks for `source`-kommandoen er:

```bash
source [options] [arguments]
```

## Common Options
- Ingen specifikke muligheder, da `source` typisk ikke har nogen indbyggede muligheder. Det tager blot stien til scriptet som argument.

## Common Examples

### Kør et script
For at køre et script, kan du bruge:

```bash
source /sti/til/script.sh
```

### Opdater miljøvariabler
Hvis du har et script, der opdaterer miljøvariabler, kan du køre det således:

```bash
source ~/.bash_profile
```

### Kør et script fra den nuværende mappe
Hvis du har et script i den nuværende mappe, kan du køre det med:

```bash
source ./mit_script.sh
```

## Tips
- Brug `source` i stedet for `./` for at sikre, at ændringer i miljøvariablerne træder i kraft i den nuværende shell.
- Sørg for, at scriptet har de nødvendige tilladelser til at blive kørt.
- Du kan også bruge `.` som en forkortelse for `source`, f.eks. `. ./mit_script.sh`.