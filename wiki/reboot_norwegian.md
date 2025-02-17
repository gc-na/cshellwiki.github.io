# [Linux] Bash reboot bruken: Gjenstart systemet

## Oversikt
`reboot`-kommandoen brukes til å gjenstarte systemet. Den avslutter alle aktive prosesser og starter datamaskinen på nytt, noe som er nyttig for å anvende systemoppdateringer eller løse problemer.

## Bruk
Grunnleggende syntaks for `reboot`-kommandoen er som følger:

```bash
reboot [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f`: Tvinger omstart uten å sende signaler til prosessene.
- `-p`: Slår av systemet etter omstart.
- `--halt`: Stopper systemet i stedet for å starte det på nytt.

## Vanlige eksempler
For å gjenstarte systemet umiddelbart, kan du bruke:

```bash
reboot
```

For å tvinge en omstart uten å vente på at prosessene skal avsluttes:

```bash
reboot -f
```

For å slå av systemet etter omstart:

```bash
reboot -p
```

## Tips
- Sørg for å lagre alt arbeid før du bruker `reboot`, da alle åpne filer og prosesser vil bli avsluttet.
- Bruk `reboot -f` med forsiktighet, da dette kan føre til datatap hvis prosesser ikke får mulighet til å avslutte ordentlig.
- Det kan være lurt å informere brukere om en planlagt omstart, spesielt på servere eller delte systemer.