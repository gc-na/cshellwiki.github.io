# [Linux] Bash cd brug: Naviger i filsystemet

## Overview
`cd` (change directory) er en Bash-kommando, der bruges til at ændre den aktuelle arbejdsmappe i terminalen. Det giver brugeren mulighed for at navigere mellem forskellige mapper i filsystemet.

## Usage
Den grundlæggende syntaks for `cd`-kommandoen er:

```bash
cd [options] [arguments]
```

## Common Options
- `..` - Gå op til den overordnede mappe.
- `-` - Skift tilbage til den forrige mappe.
- `~` - Gå til brugerens hjemmemappe.

## Common Examples
Her er nogle praktiske eksempler på, hvordan `cd` kan bruges:

1. **Gå til en specifik mappe:**
   ```bash
   cd /path/to/directory
   ```

2. **Gå op til den overordnede mappe:**
   ```bash
   cd ..
   ```

3. **Gå tilbage til den forrige mappe:**
   ```bash
   cd -
   ```

4. **Gå til hjemmemappen:**
   ```bash
   cd ~
   ```

5. **Navigere til en undermappe:**
   ```bash
   cd Documents/Projects
   ```

## Tips
- Brug `cd -` for hurtigt at skifte mellem to mapper.
- Du kan bruge tab-tasten til at autoudfylde mappenavne, hvilket sparer tid og reducerer fejl.
- For at se, hvilken mappe du befinder dig i, kan du bruge kommandoen `pwd` (print working directory) efter at have skiftet mappe.