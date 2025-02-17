# [Linux] Bash sort bruk: Sortere linjer i tekstfiler

## Oversikt
`sort`-kommandoen brukes til å sortere linjer i tekstfiler eller standard input. Den kan sortere data alfabetisk, numerisk, eller etter spesifikke felt, og er nyttig for å organisere informasjon i en mer lesbar form.

## Bruk
Den grunnleggende syntaksen for `sort`-kommandoen er:

```bash
sort [alternativer] [argumenter]
```

## Vanlige alternativer
- `-n`: Sorter numerisk.
- `-r`: Sorter i omvendt rekkefølge.
- `-k`: Angi hvilket felt som skal brukes for sortering.
- `-u`: Fjern duplikater fra sorteringen.
- `-o`: Skriv ut resultatet til en fil.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `sort`-kommandoen:

1. **Sortere en fil alfabetisk:**
   ```bash
   sort fil.txt
   ```

2. **Sortere en fil numerisk:**
   ```bash
   sort -n tall.txt
   ```

3. **Sortere i omvendt rekkefølge:**
   ```bash
   sort -r fil.txt
   ```

4. **Sortere etter et spesifikt felt:**
   Hvis du har en fil med data som er separert med mellomrom, kan du sortere etter det andre feltet:
   ```bash
   sort -k 2 fil.txt
   ```

5. **Fjerne duplikater:**
   ```bash
   sort -u fil.txt
   ```

6. **Skrive ut sortert resultat til en ny fil:**
   ```bash
   sort fil.txt -o sortert_fil.txt
   ```

## Tips
- Bruk `-n` for numeriske data for å sikre at tallene blir sortert riktig.
- Kombiner alternativer for mer spesifikke sorteringer, for eksempel `sort -n -r` for å sortere tall i omvendt rekkefølge.
- Vær oppmerksom på filens innhold og format når du bruker `-k` for å sortere etter spesifikke felt.