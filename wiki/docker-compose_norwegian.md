# [Linux] Bash docker-compose bruk: Administrer multi-container Docker-applikasjoner

## Oversikt
`docker-compose` er et verktøy som brukes til å definere og kjøre multi-container Docker-applikasjoner. Med `docker-compose` kan du enkelt konfigurere applikasjoner med flere tjenester ved hjelp av en YAML-fil, og deretter starte, stoppe og administrere disse tjenestene med enkle kommandoer.

## Bruk
Grunnleggende syntaks for `docker-compose`-kommandoen er som følger:

```bash
docker-compose [alternativer] [argumenter]
```

## Vanlige alternativer
- `up`: Starter opp tjenestene definert i `docker-compose.yml`.
- `down`: Stopper og fjerner containerne, nettverkene og volumene som er opprettet av `up`.
- `build`: Bygger eller bygger om tjenestene.
- `logs`: Viser loggene for de kjørende tjenestene.
- `exec`: Kjør en kommando i en kjørende container.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `docker-compose`:

### Starte en applikasjon
For å starte en applikasjon definert i `docker-compose.yml`, bruk:

```bash
docker-compose up
```

### Stoppe applikasjonen
For å stoppe applikasjonen og fjerne containerne, bruk:

```bash
docker-compose down
```

### Bygge tjenestene
For å bygge tjenestene på nytt, kan du bruke:

```bash
docker-compose build
```

### Vise logger
For å se loggene til de kjørende tjenestene, kjør:

```bash
docker-compose logs
```

### Kjør en kommando i en container
For å kjøre en spesifikk kommando i en kjørende container, bruk:

```bash
docker-compose exec [tjeneste] [kommando]
```
Erstatt `[tjeneste]` med navnet på tjenesten og `[kommando]` med den ønskede kommandoen.

## Tips
- Bruk `docker-compose -f [filnavn]` for å spesifisere en annen YAML-fil hvis du ikke bruker standard `docker-compose.yml`.
- Kjør `docker-compose up -d` for å starte tjenestene i bakgrunnen (detached mode).
- Hold `docker-compose.yml`-filen organisert og dokumentert for enklere vedlikehold og samarbeid med andre utviklere.