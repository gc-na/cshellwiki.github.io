# [Linux] Bash wget Bruk: Last ned filer fra nettet

## Oversikt
`wget` er et kraftig kommandolinjeverktøy som brukes til å laste ned filer fra internett. Det støtter HTTP, HTTPS og FTP-protokoller, og kan brukes til å laste ned enkeltfiler eller hele nettsteder.

## Bruk
Grunnleggende syntaks for `wget`-kommandoen er som følger:

```bash
wget [alternativer] [argumenter]
```

## Vanlige alternativer
- `-O <filnavn>`: Angi et spesifikt filnavn for den nedlastede filen.
- `-c`: Fortsett en avbrutt nedlasting.
- `-r`: Last ned filer rekursivt, nyttig for å laste ned hele nettsteder.
- `-p`: Last ned alle nødvendige filer for å vise en HTML-side, inkludert bilder og stilark.
- `--limit-rate=<hastighet>`: Sett en grense for nedlastingshastigheten.

## Vanlige eksempler
- Last ned en enkelt fil:
    ```bash
    wget https://example.com/fil.txt
    ```

- Last ned en fil med et spesifikt filnavn:
    ```bash
    wget -O nyfil.txt https://example.com/fil.txt
    ```

- Fortsett en avbrutt nedlasting:
    ```bash
    wget -c https://example.com/fil.txt
    ```

- Last ned et helt nettsted:
    ```bash
    wget -r https://example.com
    ```

- Last ned en nettside med alle nødvendige ressurser:
    ```bash
    wget -p https://example.com
    ```

## Tips
- Bruk `-q` for å kjøre `wget` i stille modus, som reduserer mengden utdata.
- Kombiner `-r` med `--no-parent` for å unngå å laste ned filer fra overordnede kataloger.
- Vær oppmerksom på serverens retningslinjer for nedlasting, og unngå å overbelaste servere med for mange forespørsel.