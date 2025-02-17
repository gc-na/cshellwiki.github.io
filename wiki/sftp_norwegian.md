# [Linux] Bash sftp bruk: Overfør filer sikkert mellom datamaskiner

## Oversikt
`sftp` (Secure File Transfer Protocol) er en interaktiv filoverføringsprotokoll som brukes til å overføre filer mellom en lokal og en ekstern datamaskin. Den tilbyr en sikker måte å overføre filer over nettverket ved å bruke SSH (Secure Shell).

## Bruk
Den grunnleggende syntaksen for `sftp`-kommandoen er:

```bash
sftp [alternativer] [brukernavn@vert]
```

## Vanlige alternativer
- `-P` : Angi portnummeret for tilkoblingen.
- `-o` : Angi spesifikke SSH-alternativer.
- `-b` : Bruk en batchfil for å kjøre flere kommandoer.
- `-r` : Overfør filer rekursivt (for kataloger).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `sftp`:

### Koble til en ekstern server
For å koble til en ekstern server med brukernavn `bruker` og vert `eksempel.com`:

```bash
sftp bruker@eksempel.com
```

### Overføre en fil fra lokal til ekstern server
For å overføre en fil kalt `fil.txt` til den eksterne serveren:

```bash
put fil.txt
```

### Overføre en fil fra ekstern til lokal server
For å laste ned en fil kalt `fil.txt` fra den eksterne serveren:

```bash
get fil.txt
```

### Overføre en katalog rekursivt
For å overføre en hel katalog kalt `min_katalog` til den eksterne serveren:

```bash
put -r min_katalog
```

### Liste filer i den eksterne katalogen
For å vise innholdet i den nåværende katalogen på den eksterne serveren:

```bash
ls
```

## Tips
- Bruk `-P` for å spesifisere en annen port hvis serveren ikke bruker standardporten 22.
- Sjekk filrettigheter og eierskap etter overføring for å sikre at de er korrekte.
- Vær oppmerksom på at `sftp` er interaktivt, så du kan bruke kommandoer som `help` for å se tilgjengelige kommandoer mens du er tilkoblet.