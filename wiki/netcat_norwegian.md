# [Linux] Bash netcat bruk: Nettverksverktøy for dataoverføring

## Oversikt
Netcat, ofte referert til som "schizofren nettverksverktøy", er et kraftig kommandolinjeverktøy som brukes til å lese og skrive data over nettverksforbindelser ved hjelp av TCP eller UDP-protokoller. Det kan brukes til en rekke oppgaver, inkludert feilsøking av nettverk, overføring av filer, og til og med som en enkel server.

## Bruk
Grunnleggende syntaks for netcat-kommandoen er som følger:

```bash
netcat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l` : Lytter på en spesifisert port for innkommende forbindelser.
- `-p` : Angir portnummeret som skal brukes.
- `-u` : Bruker UDP i stedet for TCP.
- `-v` : Aktiverer verbose-modus for mer detaljert utdata.
- `-w` : Angir tidsgrensen for tilkoblingen i sekunder.

## Vanlige eksempler

### Lytte på en port
For å starte en enkel server som lytter på port 1234, kan du bruke:

```bash
netcat -l -p 1234
```

### Koble til en server
For å koble til en server på port 80 (HTTP), kan du bruke:

```bash
netcat example.com 80
```

### Overføre en fil
For å overføre en fil fra en maskin til en annen, kan du bruke følgende kommandoer. På mottakermaskinen:

```bash
netcat -l -p 1234 > mottatt_fil.txt
```

Og på sendermaskinen:

```bash
netcat [mottaker_IP] 1234 < fil_til_send.txt
```

### Bruke UDP
For å sende en melding ved hjelp av UDP, kan du bruke:

```bash
echo "Hei, verden!" | netcat -u [mottaker_IP] 1234
```

## Tips
- Sørg for at brannmurinnstillingene tillater trafikk på de portene du bruker med netcat.
- Bruk `-v` for å få mer informasjon om tilkoblinger og feilsøking.
- Vær oppmerksom på sikkerhetsimplikasjonene ved å bruke netcat, spesielt når du lytter på porter eller overfører sensitive data.