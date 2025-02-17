# [Linux] Bash socat bruk: Kommunikasjon mellom to endepunkter

## Oversikt
`socat` (SOcket CAT) er et kraftig verktøy for å etablere toveis kommunikasjon mellom to endepunkter. Det kan brukes til å koble sammen nettverksstrømmer, filer, eller til og med terminaler, noe som gjør det til et allsidig verktøy for nettverksadministrasjon og testing.

## Bruk
Den grunnleggende syntaksen for `socat` er som følger:

```bash
socat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-u`: Bruker UDP i stedet for TCP.
- `-v`: Aktiverer verbose-modus, som gir mer detaljert informasjon om prosessen.
- `-d`: Aktiverer debug-modus for feilsøking.
- `-l`: Angir en lokal adresse for tilkoblingen.
- `-p`: Angir en port for tilkoblingen.

## Vanlige eksempler

### Eksempel 1: Koble til en TCP-server
For å koble til en TCP-server på port 1234, kan du bruke følgende kommando:

```bash
socat - TCP:localhost:1234
```

### Eksempel 2: Opprette en enkel server
For å opprette en enkel TCP-server som lytter på port 1234 og sender tilbake all data den mottar:

```bash
socat TCP-LISTEN:1234,fork -
```

### Eksempel 3: Koble to filer
For å sende innholdet fra en fil til en annen fil:

```bash
socat FILE:file1.txt FILE:file2.txt
```

### Eksempel 4: Bruke UDP
For å sende data til en UDP-server:

```bash
socat -u - UDP:localhost:1234
```

## Tips
- Bruk `-v` for å se hva som skjer under kjøringen, spesielt når du feilsøker.
- Når du oppretter servere, bruk `fork`-alternativet for å håndtere flere tilkoblinger samtidig.
- Vær oppmerksom på brannmurinnstillinger som kan blokkere portene du prøver å bruke.