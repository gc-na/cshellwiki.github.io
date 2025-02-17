# [Linux] Bash nslookup Bruk: Få DNS-informasjon

## Oversikt
`nslookup` er et nettverksverktøy som brukes til å forespørre DNS (Domain Name System) for å finne IP-adresser knyttet til domenenavn eller omvendt. Det er nyttig for feilsøking av nettverksproblemer og for å verifisere DNS-oppføringer.

## Bruk
Den grunnleggende syntaksen for `nslookup`-kommandoen er:

```
nslookup [alternativer] [argumenter]
```

## Vanlige alternativer
- `-type=TYPE`: Angir hvilken type DNS-oppføring som skal forespørres (f.eks. A, AAAA, MX).
- `-timeout=SEC`: Setter tidsavbrudd for forespørselen i sekunder.
- `-retry=N`: Angir antall ganger forespørselen skal gjentas ved feil.
- `-debug`: Viser detaljert informasjon om forespørselen og svaret.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `nslookup` kan brukes:

### Få IP-adressen til et domenenavn
```bash
nslookup www.example.com
```

### Få domenenavnet fra en IP-adresse
```bash
nslookup 93.184.216.34
```

### Spørre etter spesifikke DNS-oppføringer (f.eks. MX)
```bash
nslookup -type=MX example.com
```

### Endre DNS-server for forespørselen
```bash
nslookup www.example.com 8.8.8.8
```

## Tips
- Bruk `-debug`-alternativet for å få mer informasjon om forespørselen, noe som kan være nyttig for feilsøking.
- Når du jobber med flere DNS-servere, kan det være lurt å bruke `-retry` for å unngå unødvendige ventetider ved feil.
- Husk at `nslookup` kan gi forskjellige resultater avhengig av hvilken DNS-server du spør.