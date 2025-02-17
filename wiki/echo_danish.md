# [Linux] Bash echo brug: Udskriver tekst til terminalen

## Overview
`echo`-kommandoen bruges i Bash til at udskrive tekst eller variabler til terminalen. Det er en simpel, men nyttig kommando, der ofte anvendes i scripts og kommandolinjer for at vise information til brugeren.

## Usage
Den grundlæggende syntaks for `echo`-kommandoen er:

```bash
echo [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `echo`:

- `-n`: Undlad at udskrive en ny linje efter teksten.
- `-e`: Aktiverer fortolkning af escape-sekvenser som `\n` (ny linje) og `\t` (tab).
- `-E`: Deaktiverer fortolkning af escape-sekvenser (standardadfærd).

## Common Examples
Her er nogle praktiske eksempler på brugen af `echo`:

1. **Udskrive simpel tekst:**
   ```bash
   echo "Hej, verden!"
   ```

2. **Udskrive tekst uden ny linje:**
   ```bash
   echo -n "Dette er på samme linje."
   ```

3. **Brug af escape-sekvenser:**
   ```bash
   echo -e "Linje 1\nLinje 2"
   ```

4. **Udskrive værdien af en variabel:**
   ```bash
   navn="Alice"
   echo "Mit navn er $navn."
   ```

5. **Udskrive flere argumenter:**
   ```bash
   echo "Første argument" "Andet argument"
   ```

## Tips
- Brug `-n` for at undgå en ny linje, når du ønsker at fortsætte output på samme linje.
- Med `-e` kan du tilføje formatering til din tekst, hvilket kan være nyttigt for at gøre output mere læsbart.
- Husk at indkapsle tekst i citationstegn, hvis den indeholder mellemrum eller specialtegn.