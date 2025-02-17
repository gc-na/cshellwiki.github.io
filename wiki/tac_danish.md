# [Linux] Bash tac brug: Vend indholdet af en fil omvendt

## Overview
`tac` er et Bash-kommando, der bruges til at vise indholdet af en fil i omvendt rækkefølge. Det betyder, at den sidste linje i filen vises først, og den første linje vises sidst. Dette kan være nyttigt, når man hurtigt vil se de nyeste data eller analysere logfiler.

## Usage
Den grundlæggende syntaks for `tac` er som følger:

```bash
tac [options] [arguments]
```

## Common Options
- `-b`, `--before`: Indsæt en linje før den omvendte linje.
- `-r`, `--regex`: Behandl input som regulære udtryk.
- `-s`, `--separator`: Angiv en brugerdefineret separator mellem linjer.

## Common Examples
Her er nogle praktiske eksempler på, hvordan man bruger `tac`:

1. **Vis indholdet af en fil i omvendt rækkefølge:**
   ```bash
   tac filnavn.txt
   ```

2. **Vis indholdet af flere filer i omvendt rækkefølge:**
   ```bash
   tac fil1.txt fil2.txt
   ```

3. **Brug en brugerdefineret separator:**
   ```bash
   tac -s ',' filnavn.csv
   ```

4. **Kombiner med andre kommandoer, som f.eks. `grep`:**
   ```bash
   grep 'fejl' logfil.txt | tac
   ```

## Tips
- Brug `tac` sammen med `tail` for at se de nyeste linjer i en logfil:
  ```bash
  tail -n 10 logfil.txt | tac
  ```
- Overvej at bruge `tac` i scripts til at analysere data, der skal præsenteres i omvendt rækkefølge.
- Husk, at `tac` kun fungerer med tekstfiler, så sørg for, at filen er i det rigtige format.