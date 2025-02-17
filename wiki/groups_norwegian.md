# [Linux] Bash grupper: Vise brukergrupper

## Oversikt
`groups`-kommandoen brukes til å vise hvilke grupper en spesifikk bruker tilhører. Hvis ingen bruker spesifiseres, viser den gruppene for den nåværende brukeren. Dette kan være nyttig for å forstå brukerrettigheter og tilgangsnivåer i et Linux-miljø.

## Bruk
Grunnleggende syntaks for `groups`-kommandoen er:

```bash
groups [alternativer] [brukernavn]
```

## Vanlige alternativer
- `-h`, `--help`: Viser hjelpetekst for kommandoen.
- `-v`, `--version`: Viser versjonsinformasjon for `groups`.

## Vanlige eksempler
For å vise gruppene til den nåværende brukeren, kan du bruke:

```bash
groups
```

For å vise gruppene til en spesifikk bruker, for eksempel `john`, kan du bruke:

```bash
groups john
```

Hvis du ønsker å se hjelpeteksten for `groups`, kan du skrive:

```bash
groups --help
```

## Tips
- Bruk `groups`-kommandoen for å sjekke brukerrettigheter før du gir tilgang til sensitive filer eller kataloger.
- Kombiner `groups` med andre kommandoer som `id` for mer detaljert informasjon om brukeren og gruppene.
- Husk at du kan bruke `groups` i skript for å automatisere oppgaver som krever gruppeinformasjon.