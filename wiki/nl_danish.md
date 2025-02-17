# [Linux] Bash nl brug: nummerer linjer i tekstfiler

## Overview
`nl` er et Bash-kommando, der bruges til at nummerere linjer i tekstfiler. Det er nyttigt, når du ønsker at tilføje linjenumre til output, hvilket kan gøre det lettere at referere til specifikke linjer i filen.

## Usage
Den grundlæggende syntaks for `nl`-kommandoen er:

```bash
nl [options] [arguments]
```

## Common Options
- `-b` : Angiver, hvordan linjer skal nummereres. Mulighederne inkluderer `a` (nummerer alle linjer) og `t` (nummerer kun ikke-tomme linjer).
- `-f` : Angiver, hvilke linjer der skal nummereres, baseret på et mønster.
- `-h` : Angiver en overskrift, der skal vises før linjenumrene.
- `-n` : Bestemmer formatet for linjenumrene. Mulighederne inkluderer `ln` (venstrejusteret), `rn` (højrejusteret) og `rz` (fyldt med nuller).

## Common Examples
Her er nogle praktiske eksempler på brugen af `nl`:

1. Nummerer alle linjer i en fil:
   ```bash
   nl fil.txt
   ```

2. Nummerer kun ikke-tomme linjer:
   ```bash
   nl -b t fil.txt
   ```

3. Tilføj en overskrift før linjenumrene:
   ```bash
   nl -h "Linjenumre:" fil.txt
   ```

4. Højrejuster linjenumrene:
   ```bash
   nl -n rn fil.txt
   ```

5. Nummerer linjer med et specifikt mønster:
   ```bash
   nl -f 2 fil.txt
   ```

## Tips
- Brug `nl` i kombination med andre kommandoer som `cat` for at vise nummererede linjer i realtid:
  ```bash
  cat fil.txt | nl
  ```
- Overvej at bruge `nl` sammen med `grep` for at finde specifikke linjer i en fil med linjenumre:
  ```bash
  grep "søgeord" fil.txt | nl
  ```
- Hvis du arbejder med store filer, kan det være nyttigt at bruge `less` til at navigere i outputtet:
  ```bash
  nl fil.txt | less
  ```