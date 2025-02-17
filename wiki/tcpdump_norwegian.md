# [Linux] Bash tcpdump Bruk: Fange nettverkspakker

## Oversikt
tcpdump er et kraftig kommandolinjeverktøy som brukes til å fange og analysere nettverkspakker som passerer gjennom en datamaskins nettverksgrensesnitt. Det gir brukerne mulighet til å inspisere nettverkstrafikk i sanntid, noe som er nyttig for feilsøking og sikkerhetsanalyse.

## Bruk
Grunnleggende syntaks for tcpdump-kommandoen er som følger:

```bash
tcpdump [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-i <grensesnitt>`: Angir nettverksgrensesnittet som skal overvåkes.
- `-n`: Deaktiverer DNS-oppslag for å vise IP-adresser i stedet for vertsnavn.
- `-c <antall>`: Fanger et spesifisert antall pakker før den avslutter.
- `-w <fil>`: Skriver de fangede pakkene til en fil for senere analyse.
- `-r <fil>`: Leser pakker fra en fil i stedet for å fange dem i sanntid.

## Vanlige Eksempler
Her er noen praktiske eksempler på hvordan du kan bruke tcpdump:

1. Fange pakker på et spesifikt grensesnitt:
   ```bash
   tcpdump -i eth0
   ```

2. Fange et bestemt antall pakker:
   ```bash
   tcpdump -c 10 -i eth0
   ```

3. Fange pakker uten DNS-oppslag:
   ```bash
   tcpdump -n -i eth0
   ```

4. Skrive fangede pakker til en fil:
   ```bash
   tcpdump -w pakker.pcap -i eth0
   ```

5. Lese pakker fra en fil:
   ```bash
   tcpdump -r pakker.pcap
   ```

## Tips
- Bruk `-v`, `-vv`, eller `-vvv` for å få mer detaljert informasjon om pakkene.
- Kombiner alternativer for mer spesifikke fanger, for eksempel `tcpdump -i eth0 -n port 80` for å fange HTTP-trafikk.
- Vær oppmerksom på at tcpdump kan kreve superbrukerrettigheter, så du må kanskje bruke `sudo` for å kjøre kommandoen.