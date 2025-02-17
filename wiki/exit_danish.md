# [Linux] Bash exit brug: Afslut et script eller en shell-session

## Overview
`exit`-kommandoen bruges til at afslutte et shell-script eller en shell-session. Den returnerer en exit-status til det kaldende miljø, hvilket kan være nyttigt for at indikere, om scriptet blev udført korrekt eller ej.

## Usage
Den grundlæggende syntaks for `exit`-kommandoen er som følger:

```bash
exit [options] [status]
```

## Common Options
- `status`: En valgfri numerisk værdi, der angiver exit-status. Standardstatus er 0, hvilket betyder succes. Enhver anden værdi indikerer en fejl.

## Common Examples

1. **Afslut et script med succes**
   ```bash
   #!/bin/bash
   echo "Scriptet kører..."
   exit 0
   ```

2. **Afslut et script med en fejlstatus**
   ```bash
   #!/bin/bash
   echo "Der opstod en fejl!"
   exit 1
   ```

3. **Afslut en interaktiv shell-session**
   ```bash
   exit
   ```

4. **Afslut et script baseret på en betingelse**
   ```bash
   #!/bin/bash
   if [ -f "vigtig_fil.txt" ]; then
       echo "Fil findes."
       exit 0
   else
       echo "Fil findes ikke."
       exit 1
   fi
   ```

## Tips
- Brug `exit 0` for at indikere, at scriptet er afsluttet uden fejl.
- Brug `exit 1` eller en anden ikke-nul værdi for at indikere, at der opstod en fejl.
- Det er en god praksis at afslutte scripts med en exit-status, så andre scripts eller programmer kan håndtere resultatet korrekt.