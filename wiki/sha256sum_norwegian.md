# [Linux] Bash sha256sum Bruk: Beregn SHA-256 hash for filer

## Oversikt
`sha256sum` er et Bash-kommando som brukes til å beregne og verifisere SHA-256 hashverdier for filer. Dette er nyttig for å sikre integriteten til filer ved å sammenligne hashverdier.

## Bruk
Grunnleggende syntaks for kommandoen er som følger:

```bash
sha256sum [alternativer] [argumenter]
```

## Vanlige alternativer
- `-b`: Behandler filene i binærmodus.
- `-c`: Verifiserer hashverdier mot en fil med forventede verdier.
- `--help`: Viser hjelp og tilgjengelige alternativer for kommandoen.
- `--version`: Viser versjonsinformasjon for `sha256sum`.

## Vanlige eksempler
For å beregne SHA-256 hash for en fil:

```bash
sha256sum fil.txt
```

For å beregne hash for flere filer:

```bash
sha256sum fil1.txt fil2.txt
```

For å verifisere en fil mot en eksisterende hashverdi lagret i en tekstfil:

```bash
sha256sum -c hashfil.txt
```

For å bruke binærmodus når du beregner hash:

```bash
sha256sum -b fil.bin
```

## Tips
- Sørg for at filene du sammenligner har blitt overført eller lagret på en sikker måte for å unngå feil i hashverdiene.
- Bruk `-c` alternativet for å enkelt verifisere flere filer mot en liste med hashverdier.
- Lagre hashverdiene i en sikker fil for fremtidig verifisering av filintegritet.