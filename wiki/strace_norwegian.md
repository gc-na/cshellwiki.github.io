# [Linux] Bash strace bruk: Spore systemkall og signaler

## Oversikt
`strace` er et kraftig verktøy i Linux som brukes til å spore systemkall og signaler som et program gjør. Det gir utviklere og systemadministratorer innsikt i hvordan et program interagerer med operativsystemet, noe som er nyttig for feilsøking og ytelsesanalyse.

## Bruk
Den grunnleggende syntaksen for `strace` er som følger:

```bash
strace [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Oppsummerer systemkallene og viser statistikk.
- `-f`: Følger prosesser som opprettes av programmet.
- `-e`: Filtrerer systemkall basert på spesifikke kriterier.
- `-o <fil>`: Skriver utstrace-output til en spesifisert fil i stedet for standard utgang.
- `-p <pid>`: Sporer et allerede kjørende program ved å spesifisere prosess-ID.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `strace`:

1. **Spore et enkelt program:**
   ```bash
   strace ls
   ```

2. **Følge prosesser:**
   ```bash
   strace -f ./program
   ```

3. **Filtrere spesifikke systemkall:**
   ```bash
   strace -e trace=open,close ./program
   ```

4. **Skrive utdata til en fil:**
   ```bash
   strace -o output.txt ./program
   ```

5. **Spore en kjørende prosess:**
   ```bash
   strace -p 1234
   ```

## Tips
- Bruk `-c` for å få en oppsummering av systemkallene, noe som kan være nyttig for å identifisere flaskehalser.
- Vær oppmerksom på at `strace` kan påvirke ytelsen til programmet som spores, så det er best å bruke det i et testmiljø.
- Kombiner `strace` med andre verktøy som `grep` for å filtrere ut spesifikke systemkall i outputen.