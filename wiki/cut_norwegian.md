# [Linux] Bash cut Bruk: Hente ut deler av tekstlinjer

## Oversikt
`cut`-kommandoen brukes til å hente ut spesifikke deler av tekstlinjer fra filer eller standard input. Den er nyttig for å bearbeide tekstdata og kan brukes til å dele opp linjer basert på avgrensere eller posisjoner.

## Bruk
Den grunnleggende syntaksen for `cut`-kommandoen er:

```bash
cut [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f`: Angir feltene som skal kuttes ut, basert på en definert avgrenser.
- `-d`: Angir avgrenseren som brukes for å dele opp linjene (standard er tab).
- `-c`: Angir spesifikke tegnposisjoner som skal kuttes ut.
- `--complement`: Returnerer alt unntatt de spesifiserte feltene eller posisjonene.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `cut` kan brukes:

1. **Hente ut spesifikke felter fra en CSV-fil:**
   Hvis du har en fil `data.csv` med innhold som dette:
   ```
   navn, alder, by
   Ola, 30, Oslo
   Kari, 25, Bergen
   ```
   For å hente ut navn og by, kan du bruke:
   ```bash
   cut -d ',' -f 1,3 data.csv
   ```

2. **Hente ut spesifikke tegnposisjoner:**
   Hvis du har en tekstlinje og ønsker å hente ut de første 5 tegnene:
   ```bash
   echo "Hei på deg!" | cut -c 1-5
   ```

3. **Bruke avgrenser for å hente ut felter:**
   Anta at du har en fil `log.txt` med innhold som dette:
   ```
   2023-10-01 10:00:00 INFO Startet prosess
   2023-10-01 10:05:00 ERROR Feil oppstod
   ```
   For å hente ut dato og tid:
   ```bash
   cut -d ' ' -f 1,2 log.txt
   ```

## Tips
- Når du bruker `-d` for å spesifisere en avgrenser, husk at du kan bruke hvilken som helst karakter, for eksempel `-d ';'` for semikolon.
- Kombiner `cut` med andre kommandoer som `grep` eller `sort` for mer avansert tekstbehandling.
- Vær oppmerksom på at `cut` ikke endrer filen; den skriver bare ut resultatet til standard output. Hvis du vil lagre resultatet, kan du bruke omdirigering (`>`).