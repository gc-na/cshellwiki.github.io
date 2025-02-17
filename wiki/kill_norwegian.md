# [Linux] Bash kill bruken: Avslutte prosesser

## Oversikt
`kill`-kommandoen brukes til å sende signaler til prosesser i Unix-lignende operativsystemer. Den mest vanlige bruken er å avslutte prosesser som kjører på systemet.

## Bruk
Den grunnleggende syntaksen for `kill`-kommandoen er som følger:

```bash
kill [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l`: Viser en liste over tilgjengelige signaler.
- `-s SIGNAL`: Angir hvilket signal som skal sendes (standard er `TERM`).
- `-n SIGNAL`: Sender signalet med et nummer i stedet for navnet.

## Vanlige eksempler
For å avslutte en prosess med et spesifikt PID (prosess-ID):

```bash
kill 1234
```

For å sende et spesifikt signal, for eksempel `SIGKILL`:

```bash
kill -9 1234
```

For å sende et signal til flere prosesser samtidig:

```bash
kill 1234 5678
```

For å vise tilgjengelige signaler:

```bash
kill -l
```

## Tips
- Bruk `kill -l` for å se en liste over signaler og deres nummer.
- Vær forsiktig med `SIGKILL` (signal 9), da dette ikke gir prosessen tid til å rydde opp.
- Du kan bruke `pkill` for å avslutte prosesser basert på prosessnavn i stedet for PID.