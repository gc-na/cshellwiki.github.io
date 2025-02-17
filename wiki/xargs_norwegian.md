# [Linux] Bash xargs Bruk: Behandle standard input som argumenter

## Oversikt
`xargs` er et kraftig Bash-verktøy som brukes til å bygge og kjøre kommandoer fra standard input. Det tar input fra stdin og konverterer det til argumenter for en annen kommando, noe som gjør det nyttig for å håndtere store mengder data.

## Bruk
Grunnleggende syntaks for `xargs` er som følger:

```bash
xargs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-n N`: Angir hvor mange argumenter som skal sendes til kommandoen per gang.
- `-d DELIM`: Spesifiserer en tilpasset avgrenser for input.
- `-0`: Behandler input som null-terminerte strenger, nyttig for filnavn med mellomrom.
- `-p`: Ber om bekreftelse før hver kommando kjøres.
- `-I {}`: Angir en plassholder for hvor input skal settes inn i kommandoen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `xargs` kan brukes:

### Eksempel 1: Fjerne filer
Fjern alle `.tmp`-filer i en katalog:

```bash
find . -name "*.tmp" | xargs rm
```

### Eksempel 2: Kopiere filer
Kopier alle `.jpg`-filer til en annen katalog:

```bash
ls *.jpg | xargs -I {} cp {} /path/to/destination/
```

### Eksempel 3: Bruke en tilpasset avgrenser
Bruk `-d` for å spesifisere en tilpasset avgrenser:

```bash
echo "file1,file2,file3" | xargs -d ',' rm
```

### Eksempel 4: Be om bekreftelse
Kjør en kommando med bekreftelse før hver utførelse:

```bash
echo "file1 file2 file3" | xargs -p rm
```

## Tips
- Bruk `-0` sammen med `find` for å håndtere filnavn med mellomrom eller spesialtegn.
- Kombiner `xargs` med `find` for å effektivt håndtere store mengder filer.
- Vær forsiktig med `rm`-kommandoen; test alltid med `echo` først for å se hvilke filer som vil bli påvirket.