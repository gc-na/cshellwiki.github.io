# [Linux] Bash dig Bruk: Hente DNS-informasjon

## Oversikt
`dig` (Domain Information Groper) er et kommandolinjeverktøy som brukes til å hente DNS-informasjon om domener. Det er nyttig for feilsøking av DNS-problemer og for å få detaljerte opplysninger om DNS-poster.

## Bruk
Grunnleggende syntaks for `dig`-kommandoen er som følger:

```
dig [alternativer] [argumenter]
```

## Vanlige alternativer
- `@server`: Spesifiserer en DNS-server for forespørselen.
- `-t type`: Angir typen DNS-post som skal hentes (f.eks. A, AAAA, MX).
- `+short`: Viser en kortere, mer konsis utdata.
- `+trace`: Følger DNS-oppslagstrinnene for å vise hvordan forespørselen blir behandlet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `dig`:

1. Hente A-posten for et domene:
   ```bash
   dig example.com
   ```

2. Hente MX-poster for et domene:
   ```bash
   dig -t MX example.com
   ```

3. Spørre en spesifikk DNS-server:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. Vise en kortere utgave av A-posten:
   ```bash
   dig +short example.com
   ```

5. Følge DNS-oppslagstrinnene:
   ```bash
   dig +trace example.com
   ```

## Tips
- Bruk `+short` for å få en mer oversiktlig utdata når du bare trenger den grunnleggende informasjonen.
- Når du feilsøker DNS-problemer, kan det være nyttig å bruke `+trace` for å se hele oppslagsprosessen.
- Husk å spesifisere DNS-serveren hvis du mistenker at den lokale serveren kan være feilkonfigurert.