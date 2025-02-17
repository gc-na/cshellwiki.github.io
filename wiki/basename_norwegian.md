# [Linux] Bash basename bruk: Hent filnavn fra en sti

## Oversikt
`basename`-kommandoen brukes til å hente filnavnet fra en full filbane. Den fjerner eventuelle prefikser og gir deg bare navnet på filen eller katalogen.

## Bruk
Grunnleggende syntaks for `basename`-kommandoen er som følger:

```bash
basename [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Behandle flere filer og returnere filnavnene for hver av dem.
- `-s`: Angi et suffiks som skal fjernes fra filnavnet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `basename`:

1. Hente filnavnet fra en full sti:
   ```bash
   basename /path/to/file.txt
   ```
   Utdata: `file.txt`

2. Hente filnavnet uten suffiks:
   ```bash
   basename /path/to/file.txt .txt
   ```
   Utdata: `file`

3. Behandle flere filer samtidig:
   ```bash
   basename -a /path/to/file1.txt /path/to/file2.txt
   ```
   Utdata:
   ```
   file1.txt
   file2.txt
   ```

4. Fjerne et spesifikt suffiks fra flere filer:
   ```bash
   basename -s .txt /path/to/file1.txt /path/to/file2.txt
   ```
   Utdata:
   ```
   file1
   file2
   ```

## Tips
- Bruk `basename` når du jobber med skript for å gjøre filnavn mer lesbare.
- Kombiner `basename` med andre kommandoer som `find` for å håndtere filnavn dynamisk.
- Vær oppmerksom på at `basename` ikke håndterer stier med mellomrom eller spesialtegn uten riktig escaping.