# [Linux] Bash rev: Vend tekstlinjer om

## Overview
`rev` er et Bash-kommando, der bruges til at vende teksten i hver linje af en fil eller fra standard input. Det betyder, at det tager de enkelte linjer og reverserer rækkefølgen af tegnene, hvilket kan være nyttigt til forskellige tekstbehandlingsopgaver.

## Usage
Den grundlæggende syntaks for `rev`-kommandoen er:

```bash
rev [options] [arguments]
```

## Common Options
- `-o, --output=FILE`: Angiv en outputfil, hvor den omvendte tekst skal gemmes.
- `-h, --help`: Vis hjælp og afslut.
- `-V, --version`: Vis versionsinformation og afslut.

## Common Examples
Her er nogle praktiske eksempler på, hvordan `rev` kan bruges:

1. **Vend tekst fra standard input:**
   ```bash
   echo "Hej Verden" | rev
   ```
   Output:
   ```
   nedreV jeH
   ```

2. **Vend indholdet af en fil:**
   ```bash
   rev fil.txt
   ```

3. **Gem den omvendte tekst i en ny fil:**
   ```bash
   rev fil.txt -o omvendt_fil.txt
   ```

4. **Brug `rev` i en pipeline:**
   ```bash
   cat fil.txt | rev | sort
   ```

## Tips
- `rev` kan være nyttig i scripts, hvor du har brug for at manipulere tekstdata.
- Kombiner `rev` med andre kommandoer som `sort` eller `uniq` for at opnå mere komplekse tekstbehandlingsopgaver.
- Husk at `rev` kun vender tegnene i hver linje, ikke hele filens rækkefølge.