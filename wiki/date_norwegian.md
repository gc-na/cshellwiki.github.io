# [Linux] Bash date bruk: Hente og formatere dato og tid

## Oversikt
`date`-kommandoen brukes til å vise og formatere dato og tid i Linux. Den kan også brukes til å sette systemets dato og tid, avhengig av brukerens tillatelser.

## Bruk
Grunnleggende syntaks for `date`-kommandoen er som følger:

```bash
date [alternativer] [argumenter]
```

## Vanlige alternativer
- `+FORMAT`: Angi formatet for utdataene. For eksempel, `%Y` for år, `%m` for måned, `%d` for dag.
- `-u`: Vis dato og tid i UTC (Coordinated Universal Time).
- `-d STRING`: Vis dato og tid for en spesifisert streng. For eksempel, `-d "next Friday"`.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `date`-kommandoen kan brukes:

1. **Vis dagens dato og tid:**
   ```bash
   date
   ```

2. **Vis dato i spesifikt format:**
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. **Vis dato i UTC:**
   ```bash
   date -u
   ```

4. **Vis dato for neste fredag:**
   ```bash
   date -d "next Friday"
   ```

5. **Sett systemdato (krever root-rettigheter):**
   ```bash
   sudo date -s "2023-10-01 12:00:00"
   ```

## Tips
- Bruk `date +%F` for å få datoen i ISO-format (YYYY-MM-DD), som er nyttig for skripting.
- Kombiner `date` med andre kommandoer ved å bruke backticks eller `$()`, for eksempel: 
  ```bash
  echo "Backup started at $(date +%Y-%m-%d_%H-%M-%S)"
  ```
- Husk at endring av systemdato og tid kan påvirke kjørende tjenester, så vær forsiktig når du bruker `sudo date -s`.