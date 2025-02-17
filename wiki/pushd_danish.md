# [Linux] Bash pushd brug: Skift mellem mapper

## Overview
`pushd` er en Bash-kommando, der bruges til at skifte mellem mapper og samtidig gemme den nuværende mappe på en stak. Dette gør det muligt for brugeren nemt at navigere tilbage til tidligere mapper.

## Usage
Den grundlæggende syntaks for `pushd` er som følger:

```bash
pushd [options] [arguments]
```

## Common Options
- `+n`: Gå til den n-te mappe i stakken.
- `-n`: Skift til den sidste mappe uden at ændre stakken.
- `-`: Skift tilbage til den forrige mappe.

## Common Examples
Her er nogle praktiske eksempler på, hvordan `pushd` kan bruges:

1. Skift til en ny mappe og gem den nuværende mappe:
   ```bash
   pushd /path/to/new/directory
   ```

2. Gå tilbage til den tidligere mappe:
   ```bash
   pushd -
   ```

3. Gå til den anden mappe i stakken:
   ```bash
   pushd +1
   ```

4. Skift til en mappe og vis stakken:
   ```bash
   pushd /another/directory && dirs
   ```

## Tips
- Brug `dirs` for at se stakken af mapper, så du kan holde styr på, hvor du har været.
- Kombiner `pushd` med `popd` for at navigere effektivt mellem mapper. `popd` fjerner den øverste mappe fra stakken og skifter tilbage til den forrige.
- Overvej at bruge `pushd` i scripts for at gøre din mappe-navigation mere struktureret og effektiv.