# [Linux] Bash ss bruk: Vise nettverksforbindelser

## Oversikt
`ss` (socket statistics) er et verktøy i Linux som brukes til å vise detaljerte informasjon om nettverksforbindelser, inkludert TCP, UDP, og UNIX-sokler. Det gir en raskere og mer omfattende oversikt over tilkoblinger sammenlignet med det eldre `netstat`-verktøyet.

## Bruk
Grunnleggende syntaks for `ss`-kommandoen er som følger:

```bash
ss [alternativer] [argumenter]
```

## Vanlige alternativer
- `-t`: Vis kun TCP-forbindelser.
- `-u`: Vis kun UDP-forbindelser.
- `-l`: Vis kun lytteforbindelser.
- `-p`: Vis prosessinformasjon knyttet til forbindelsene.
- `-n`: Vis numeriske adresser og porter i stedet for å prøve å løse dem til navn.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `ss` kan brukes:

1. **Vis alle aktive forbindelser:**
   ```bash
   ss
   ```

2. **Vis kun TCP-forbindelser:**
   ```bash
   ss -t
   ```

3. **Vis lytteforbindelser:**
   ```bash
   ss -l
   ```

4. **Vis UDP-forbindelser med prosessinformasjon:**
   ```bash
   ss -u -p
   ```

5. **Vis alle forbindelser med numeriske adresser:**
   ```bash
   ss -n
   ```

## Tips
- Bruk `ss -t -a` for å vise alle aktive TCP-forbindelser, både lytte- og etablerte forbindelser.
- Kombiner alternativer for mer spesifik informasjon, for eksempel `ss -tunlp` for å vise både TCP og UDP, lytteforbindelser, og prosessinformasjon.
- `ss` kan være nyttig for feilsøking av nettverksproblemer, så vær oppmerksom på tilkoblinger som kan være uventede eller mistenkelige.