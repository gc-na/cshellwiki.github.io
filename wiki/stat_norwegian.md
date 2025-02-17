# [Linux] Bash stat Bruk: Hent filstatistikk

## Oversikt
`stat`-kommandoen brukes til å vise detaljerte informasjon om filer og kataloger i Linux. Den gir informasjon som filstørrelse, eierskap, tillatelser, og tidsstempler for opprettelse, endring og tilgang.

## Bruk
Den grunnleggende syntaksen for `stat`-kommandoen er som følger:

```bash
stat [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-c` : Angi et format for utdataene.
- `-f` : Vis informasjon om filsystemet i stedet for filen.
- `--help` : Vis hjelpemeldinger for kommandoen.
- `--version` : Vis versjonsinformasjon for `stat`.

## Vanlige Eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `stat`-kommandoen:

1. **Vis informasjon om en fil:**
   ```bash
   stat filnavn.txt
   ```

2. **Vis informasjon om en katalog:**
   ```bash
   stat /path/to/directory
   ```

3. **Bruke formatalternativet for spesifikke detaljer:**
   ```bash
   stat -c '%s %y' filnavn.txt
   ```
   Dette viser filstørrelsen og den siste endringstiden.

4. **Vis informasjon om filsystemet:**
   ```bash
   stat -f /
   ```

## Tips
- Bruk `-c` alternativet for å tilpasse utdataene til dine behov.
- Kombiner `stat` med andre kommandoer ved hjelp av rør (`|`) for å filtrere eller formatere utdataene ytterligere.
- Husk at `stat` kan gi deg nyttig informasjon som kan være nyttig for feilsøking av fil- og katalogproblemer.