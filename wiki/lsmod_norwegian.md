# [Linux] Bash lsmod bruksområde: Vise lastede moduler

## Oversikt
`lsmod` er et Bash-kommando som brukes til å vise en liste over lastede kjerne-moduler i Linux-operativsystemet. Dette verktøyet gir en oversikt over hvilke moduler som er aktive, noe som kan være nyttig for feilsøking og systemadministrasjon.

## Bruk
Den grunnleggende syntaksen for `lsmod` er som følger:

```bash
lsmod [alternativer] [argumenter]
```

## Vanlige alternativer
`lsmod` har ikke mange alternativer, men her er de mest brukte:

- Ingen alternativer: `lsmod` kjøres uten alternativer for å vise alle lastede moduler.
- `-h`, `--help`: Viser hjelpetekst med tilgjengelige alternativer.

## Vanlige eksempler

For å vise alle lastede moduler, kan du ganske enkelt kjøre:

```bash
lsmod
```

For å filtrere ut spesifikke moduler, kan du bruke `grep` i kombinasjon med `lsmod`. For eksempel, for å finne moduler relatert til nettverk:

```bash
lsmod | grep net
```

Du kan også bruke `less` for å bla gjennom lange lister:

```bash
lsmod | less
```

## Tips
- Bruk `lsmod` i kombinasjon med andre kommandoer som `modinfo` for å få mer informasjon om spesifikke moduler.
- Vær oppmerksom på at `lsmod` kun viser moduler som er lastet inn i kjernen; det viser ikke moduler som er tilgjengelige, men ikke lastet.
- For mer detaljert informasjon om modulene, kan du bruke `modprobe -l` for å liste alle tilgjengelige moduler.