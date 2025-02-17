# [Linux] Bash curl bruk: Hente data fra nettverk

## Oversikt
`curl` er et kommandolinjeverktøy som brukes til å overføre data til eller fra en server ved hjelp av ulike protokoller, inkludert HTTP, HTTPS, FTP og mer. Det er spesielt nyttig for å hente innhold fra nettadresser eller for å sende data til en server.

## Bruk
Grunnleggende syntaks for `curl`-kommandoen er som følger:
```bash
curl [alternativer] [argumenter]
```

## Vanlige alternativer
- `-X`: Angi HTTP-metoden (f.eks. GET, POST).
- `-d`: Send data i en POST-forespørsel.
- `-H`: Legg til en HTTP-header.
- `-o`: Lagre output til en fil.
- `-I`: Hent bare HTTP-headerne fra en URL.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `curl`:

### Hente en nettside
```bash
curl https://www.example.com
```

### Hente bare HTTP-headerne
```bash
curl -I https://www.example.com
```

### Sende en POST-forespørsel med data
```bash
curl -X POST -d "name=John&age=30" https://www.example.com/api
```

### Legge til en HTTP-header
```bash
curl -H "Authorization: Bearer token" https://www.example.com/protected
```

### Lagre output til en fil
```bash
curl -o filnavn.html https://www.example.com
```

## Tips
- Bruk `-v` for å få mer detaljert informasjon om forespørselen og svaret, noe som kan være nyttig for feilsøking.
- Når du sender sensitive data, vurder å bruke `https` for å sikre overføringen.
- Du kan kombinere flere alternativer i én kommando for mer komplekse forespørseler.