# [Linux] Bash mpstat Bruk: Overvåking av prosessorbruk

## Oversikt
`mpstat` er et verktøy som brukes til å overvåke prosessoraktivitet på systemet. Det gir detaljerte statistikker om CPU-bruk, inkludert informasjon om hver enkelt prosessor, noe som er nyttig for ytelsesanalyse og feilsøking.

## Bruk
Grunnleggende syntaks for `mpstat`-kommandoen er som følger:

```bash
mpstat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-P ALL`: Viser statistikk for alle prosessorer.
- `-u`: Viser CPU-bruk i prosent.
- `-h`: Viser utdata i et mer lesbart format.
- `-o`: Angir utdataformatet (f.eks. CSV).
- `interval`: Angir hvor ofte statistikken skal oppdateres, i sekunder.
- `count`: Antall ganger statistikken skal vises.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `mpstat`:

1. **Vis statistikk for alle prosessorer:**
   ```bash
   mpstat -P ALL
   ```

2. **Vis CPU-bruk hvert 2. sekund i 5 sekunder:**
   ```bash
   mpstat 2 5
   ```

3. **Vis CPU-bruk med lesbart format:**
   ```bash
   mpstat -h
   ```

4. **Lagre utdata til en CSV-fil:**
   ```bash
   mpstat -o CSV 1 10 > cpu_usage.csv
   ```

## Tips
- Bruk `mpstat -P ALL` for å få en helhetlig oversikt over alle prosessorer, spesielt på systemer med flere kjerner.
- Kombiner `mpstat` med andre verktøy som `grep` for å filtrere ut spesifikke prosessorer eller verdier.
- Vurder å bruke `mpstat` i skript for å overvåke CPU-bruk over tid og samle data for analyse.