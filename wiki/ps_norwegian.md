# [Linux] Bash ps Bruk: Vise prosesser

## Oversikt
`ps`-kommandoen brukes til å vise informasjon om aktive prosesser på systemet. Den gir en oversikt over hvilke prosesser som kjører, deres prosess-ID (PID), og annen relevant informasjon som minnebruk og CPU-bruk.

## Bruk
Grunnleggende syntaks for `ps`-kommandoen er som følger:

```bash
ps [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e` eller `-A`: Viser alle prosesser.
- `-f`: Viser full formatert informasjon om prosessene.
- `-u [brukernavn]`: Viser prosesser for en spesifikk bruker.
- `-aux`: Viser alle prosesser med detaljert informasjon.
- `--sort`: Sorterer prosessene etter spesifiserte kriterier.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `ps` kan brukes:

1. Vise alle prosesser:
   ```bash
   ps -e
   ```

2. Vise prosesser med full formatert informasjon:
   ```bash
   ps -f
   ```

3. Vise prosesser for en spesifikk bruker:
   ```bash
   ps -u brukernavn
   ```

4. Vise alle prosesser med detaljert informasjon:
   ```bash
   ps aux
   ```

5. Sortere prosessene etter minnebruk:
   ```bash
   ps aux --sort=-%mem
   ```

## Tips
- Bruk `man ps` for å få mer detaljert informasjon om tilgjengelige alternativer og bruksområder.
- Kombiner `ps` med `grep` for å filtrere prosesser. For eksempel:
  ```bash
  ps aux | grep prosessnavn
  ```
- Vær oppmerksom på at `ps` viser en øyeblikksbilde av prosessene, så informasjonen kan endre seg raskt.