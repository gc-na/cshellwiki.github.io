# [Linux] Bash ftp Bruk: Overføre filer via FTP

## Oversikt
`ftp`-kommandoen brukes til å overføre filer mellom datamaskiner over et nettverk ved hjelp av File Transfer Protocol (FTP). Den gir en interaktiv måte å laste opp og laste ned filer fra en FTP-server.

## Bruk
Den grunnleggende syntaksen for `ftp`-kommandoen er:

```bash
ftp [alternativer] [vert]
```

## Vanlige Alternativer
- `-i`: Slå av interaktiv modus, som hindrer prompt for hver filoverføring.
- `-n`: Forhindre automatisk innlogging til FTP-serveren.
- `-v`: Aktiver detaljert modus, som viser mer informasjon om overføringer.

## Vanlige Eksempler
Her er noen praktiske eksempler på hvordan du bruker `ftp`-kommandoen:

### Koble til en FTP-server
For å koble til en FTP-server, bruk følgende kommando:

```bash
ftp ftp.example.com
```

### Laste opp en fil
For å laste opp en fil til serveren, bruk `put`-kommandoen etter at du har logget inn:

```bash
put lokal_fil.txt
```

### Laste ned en fil
For å laste ned en fil fra serveren, bruk `get`-kommandoen:

```bash
get fjern_fil.txt
```

### Liste filer på serveren
For å vise filer i den nåværende katalogen på serveren, bruk:

```bash
ls
```

## Tips
- Bruk `-n` alternativet hvis du ønsker å spesifisere brukernavn og passord manuelt etter tilkobling.
- Husk å bruke `bye`-kommandoen for å avslutte FTP-økten på en sikker måte.
- Vær oppmerksom på at FTP overfører data i klartekst; vurder å bruke SFTP for mer sikkerhet.