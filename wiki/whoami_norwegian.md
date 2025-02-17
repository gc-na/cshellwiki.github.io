# [Linux] Bash whoami Bruk: Hent brukernavnet til den nåværende brukeren

## Oversikt
`whoami` er en enkel Bash-kommando som viser brukernavnet til den nåværende brukeren som er logget inn på systemet. Dette kan være nyttig for å bekrefte hvilken bruker du jobber som, spesielt når du har flere brukere eller når du bruker sudo-kommandoen.

## Bruk
Grunnleggende syntaks for kommandoen er:

```bash
whoami [alternativer]
```

## Vanlige Alternativer
`whoami` har ikke mange alternativer, men her er noen nyttige:

- `--help`: Viser hjelp og informasjon om kommandoen.
- `--version`: Viser versjonsinformasjon om `whoami`.

## Vanlige Eksempler

1. **Vis brukernavnet til den nåværende brukeren:**

   ```bash
   whoami
   ```

2. **Vis hjelp for kommandoen:**

   ```bash
   whoami --help
   ```

3. **Vis versjonsinformasjon:**

   ```bash
   whoami --version
   ```

## Tips
- Bruk `whoami` etter å ha kjørt `sudo` for å bekrefte hvilken bruker du er logget inn som etter å ha fått administrative rettigheter.
- Kombiner `whoami` med andre kommandoer i skript for å tilpasse oppførselen basert på den nåværende brukeren.
- Husk at `whoami` alltid returnerer navnet på den aktive brukeren, så det kan være nyttig å bruke det i feilsøking.