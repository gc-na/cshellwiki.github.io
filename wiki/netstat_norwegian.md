# [Linux] Bash netstat bruk: Vise nettverksforbindelser

## Oversikt
`netstat` er et kommandolinjeverktøy som brukes til å vise nettverksforbindelser, rutingtabeller, grensesnittstatistikk og mer. Det gir en oversikt over aktive nettverksforbindelser og kan være nyttig for feilsøking av nettverksproblemer.

## Bruk
Grunnleggende syntaks for `netstat`-kommandoen er som følger:

```
netstat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser alle forbindelser og lytteporter.
- `-t`: Viser TCP-forbindelser.
- `-u`: Viser UDP-forbindelser.
- `-n`: Viser adresser og porter i numerisk format.
- `-l`: Viser kun lytteporter.
- `-p`: Viser prosess-ID og programnavn som bruker forbindelsen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `netstat` kan brukes:

### Vise alle aktive forbindelser
```bash
netstat -a
```

### Vise kun TCP-forbindelser
```bash
netstat -t
```

### Vise kun UDP-forbindelser
```bash
netstat -u
```

### Vise forbindelser med numeriske adresser
```bash
netstat -n
```

### Vise lytteporter
```bash
netstat -l
```

### Vise prosessinformasjon
```bash
netstat -p
```

## Tips
- Kombiner alternativer for mer spesifikke resultater, for eksempel `netstat -tuln` for å vise alle lytte TCP- og UDP-porter i numerisk format.
- Bruk `grep` for å filtrere resultater, som i `netstat -a | grep LISTEN` for å finne lytteporter.
- Kjør `netstat` med `sudo` for å få mer detaljert informasjon om prosesser som bruker nettverksforbindelser.