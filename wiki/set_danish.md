# [Linux] Bash set brug: Konfigurer shell-indstillinger

## Overview
`set`-kommandoen i Bash bruges til at ændre indstillingerne for shellens opførsel. Det kan bruges til at aktivere eller deaktivere forskellige funktioner, som påvirker, hvordan shellen håndterer input og output, samt hvordan den udfører scripts.

## Usage
Den grundlæggende syntaks for `set`-kommandoen er som følger:

```bash
set [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `set`:

- `-e`: Stop udførelsen af scriptet, hvis en kommando returnerer en fejlkode.
- `-u`: Behandl ubestemte variabler som en fejl.
- `-x`: Vis kommandoer og deres argumenter, når de udføres (debugging).
- `-o option`: Aktiverer en specifik shell-indstilling, som kan være `noclobber`, `pipefail`, osv.

## Common Examples
Her er nogle praktiske eksempler på brugen af `set`:

1. Stop scriptet ved fejl:
   ```bash
   set -e
   ```

2. Aktivér debugging for at se, hvilke kommandoer der køres:
   ```bash
   set -x
   ```

3. Behandl ubestemte variabler som fejl:
   ```bash
   set -u
   ```

4. Kombiner flere indstillinger:
   ```bash
   set -eux
   ```

## Tips
- Brug `set -e` i scripts for at undgå, at de fortsætter ved fejl, hvilket kan føre til uventede resultater.
- Aktiver `set -x` under fejlfinding for at få indsigt i, hvordan dit script udføres.
- Husk at deaktivere debugging med `set +x`, når du er færdig med fejlfinding for at undgå unødvendig output.