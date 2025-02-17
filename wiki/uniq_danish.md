# [Linux] Bash uniq brug: Fjerner duplikater fra en sorteret liste

## Overview
`uniq`-kommandoen bruges til at fjerne duplikerede linjer fra en sorteret tekstfil eller input. Den viser kun unikke linjer, hvilket gør den nyttig til at rense data og analysere indhold.

## Usage
Den grundlæggende syntaks for `uniq`-kommandoen er som følger:

```bash
uniq [options] [arguments]
```

## Common Options
- `-c`: Tæller antallet af forekomster af hver unik linje.
- `-d`: Viser kun de linjer, der er duplikeret.
- `-u`: Viser kun de linjer, der er unikke (ikke duplikerede).
- `-i`: Ignorerer forskelle i store og små bogstaver.
- `-w N`: Ignorerer de første N tegn i hver linje, når der sammenlignes.

## Common Examples
Her er nogle praktiske eksempler på, hvordan `uniq` kan bruges:

1. **Fjerne duplikater fra en fil:**
   ```bash
   uniq fil.txt
   ```

2. **Tælle forekomster af hver unik linje:**
   ```bash
   uniq -c fil.txt
   ```

3. **Vis kun duplikerede linjer:**
   ```bash
   uniq -d fil.txt
   ```

4. **Vis kun unikke linjer:**
   ```bash
   uniq -u fil.txt
   ```

5. **Ignorer store og små bogstaver:**
   ```bash
   uniq -i fil.txt
   ```

## Tips
- Sørg for, at inputdataene er sorteret, da `uniq` kun fjerner på hinanden følgende duplikater.
- Du kan kombinere `uniq` med `sort` for at sikre, at dataene er sorteret, før du fjerner duplikater:
  ```bash
  sort fil.txt | uniq
  ```
- Brug `-w`-optionen, hvis du kun vil sammenligne en del af linjerne, hvilket kan være nyttigt i visse databehandlingsscenarier.