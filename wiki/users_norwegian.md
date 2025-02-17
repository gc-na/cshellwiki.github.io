# [Linux] Bash-brukere kommando: Hente brukeropplysninger

## Oversikt
Kommandoen `users` viser en liste over brukernavnene til de som er logget inn på systemet. Dette kan være nyttig for å få en rask oversikt over aktive brukere.

## Bruk
Den grunnleggende syntaksen for kommandoen er:

```
users [alternativer]
```

## Vanlige alternativer
- `-n`: Vis bare unike brukernavn.
- `-r`: Vis brukernavnene i en tilfeldig rekkefølge.

## Vanlige eksempler
For å vise alle brukerne som er logget inn på systemet, kan du bruke:

```bash
users
```

For å vise unike brukernavn, kan du bruke:

```bash
users -n
```

For å vise brukernavnene i tilfeldig rekkefølge, kan du bruke:

```bash
users -r
```

## Tips
- Bruk `who`-kommandoen for mer detaljert informasjon om brukerne, inkludert innloggingsdato og -tid.
- Kombiner `users` med andre kommandoer som `wc -l` for å telle antall aktive brukere:

```bash
users | wc -l
```