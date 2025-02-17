# [Linux] Bash cut brug: Skær tekstlinjer

## Oversigt
`cut`-kommandoen bruges til at udtrække sektioner fra hver linje i en tekstfil eller fra standard input. Det er nyttigt til at isolere bestemte kolonner eller felter i data.

## Brug
Den grundlæggende syntaks for `cut`-kommandoen er:

```bash
cut [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`: Angiver hvilke felter der skal udtrækkes. Felterne adskilles typisk af tabulatorer eller et specificeret tegn.
- `-d`: Angiver det tegn, der bruges som feltseparator. Standardseparatoren er tabulator.
- `-c`: Angiver hvilke tegn der skal udtrækkes fra hver linje.
- `--complement`: Udtrækker alt undtagen de angivne felter eller tegn.

## Almindelige eksempler

1. **Udtræk felter fra en fil**:
   For at udtrække det første og tredje felt fra en fil, der bruger komma som separator:
   ```bash
   cut -d ',' -f 1,3 filnavn.csv
   ```

2. **Udtræk tegn fra en tekstlinje**:
   For at udtrække de første 5 tegn fra hver linje:
   ```bash
   cut -c 1-5 filnavn.txt
   ```

3. **Udtræk alle felter undtagen det andet**:
   For at udtrække alle felter undtagen det andet fra en tabulator-separeret fil:
   ```bash
   cut --complement -f 2 filnavn.txt
   ```

4. **Brug af standard input**:
   Du kan også bruge `cut` med standard input. For eksempel, hvis du vil udtrække det første felt fra outputtet af en kommando:
   ```bash
   echo -e "a\tb\tc" | cut -f 1
   ```

## Tips
- Når du bruger `-d` til at angive en separator, skal du sørge for at vælge et tegn, der ikke optræder i dataene for at undgå utilsigtede resultater.
- Brug `-s` for at undgå at vise linjer uden det angivne felt, hvilket kan være nyttigt for at holde output rent.
- Kombiner `cut` med andre kommandoer som `sort` og `uniq` for at analysere og rense data effektivt.