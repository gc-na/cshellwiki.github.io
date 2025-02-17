# [Linux] Bash top bruk: Viser systemprosessinformasjon i sanntid

## Oversikt
`top`-kommandoen brukes til å vise en dynamisk, sanntidsvisning av systemprosesser. Den gir informasjon om hvilke prosesser som kjører, hvor mye ressurser de bruker, og lar brukeren overvåke systemets ytelse.

## Bruk
Den grunnleggende syntaksen for `top`-kommandoen er:

```
top [alternativer]
```

## Vanlige alternativer
- `-d <sekunder>`: Angir oppdateringsfrekvensen for visningen i sekunder.
- `-u <brukernavn>`: Viser bare prosessene som tilhører den spesifiserte brukeren.
- `-p <PID>`: Viser bare prosessen med den spesifiserte prosess-ID-en.

## Vanlige eksempler
For å starte `top`, kan du ganske enkelt skrive:

```
top
```

For å oppdatere visningen hvert 2. sekund, kan du bruke:

```
top -d 2
```

For å vise prosessene til en spesifikk bruker, for eksempel "john", kan du bruke:

```
top -u john
```

For å overvåke en spesifikk prosess med prosess-ID 1234, kan du bruke:

```
top -p 1234
```

## Tips
- Trykk `h` mens `top` kjører for å få hjelp om tilgjengelige kommandoer.
- Bruk `Shift + M` for å sortere prosessene etter minnebruk.
- Trykk `q` for å avslutte `top`-visningen.