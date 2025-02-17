# [Linux] Bash vigr Bruk: Rediger systemets visningsfiler

## Oversikt
`vigr` er et Bash-kommando som brukes til å redigere systemets visningsfiler, som `/etc/group` og `/etc/passwd`, på en sikker måte. Den åpner filene i en tekstredigerer, men sikrer at endringer ikke blir lagret hvis det oppstår problemer under redigeringen.

## Bruk
Den grunnleggende syntaksen for `vigr` er:

```bash
vigr [alternativer] [fil]
```

## Vanlige alternativer
- `-s`: Kjør `vigr` i sikker modus, som låser filene for redigering.
- `-f <fil>`: Spesifiser en annen fil å redigere enn standard.

## Vanlige eksempler
For å redigere `/etc/passwd`-filen, kan du bruke:

```bash
vigr /etc/passwd
```

For å redigere `/etc/group`-filen, kan du bruke:

```bash
vigr /etc/group
```

For å kjøre `vigr` i sikker modus, kan du bruke:

```bash
vigr -s
```

For å spesifisere en annen fil, kan du bruke:

```bash
vigr -f /path/to/custom/file
```

## Tips
- Bruk `vigr` i stedet for vanlige tekstredigerere for å unngå problemer med filintegritet.
- Sørg for å ha nødvendige rettigheter (vanligvis root) for å redigere systemfiler.
- Vær forsiktig med endringer i systemfiler, da feil kan føre til systemproblemer.