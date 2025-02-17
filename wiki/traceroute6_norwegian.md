# [Linux] Bash traceroute6 Bruk: Spore IPv6-nettverksruter

## Oversikt
`traceroute6` er et verktøy som brukes til å spore ruten som datapakker tar fra en kilde til en destinasjon over et IPv6-nettverk. Det gir informasjon om hver "hopp" pakken tar, inkludert IP-adressene til rutere og tiden det tar å nå hver ruter.

## Bruk
Den grunnleggende syntaksen for `traceroute6` er som følger:

```bash
traceroute6 [alternativer] [mål]
```

## Vanlige alternativer
- `-m <hopp>`: Angir maksimal antall hopp som skal spores.
- `-p <port>`: Spesifiserer portnummeret som skal brukes for UDP-pakker.
- `-w <sekunder>`: Setter tidsgrensen for å vente på svar fra hver ruter.
- `-n`: Bruker numeriske IP-adresser i stedet for å forsøke å løse dem til vertsnavn.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `traceroute6`:

1. Spore ruten til en spesifikk IPv6-adresse:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Spore ruten med en maksimal antall hopp på 15:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. Spore ruten og bruke numeriske IP-adresser:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

4. Spore ruten med en spesifikk port:
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

## Tips
- Bruk `-n` alternativet for raskere resultater, spesielt hvis du ikke trenger vertsnavn.
- Vær oppmerksom på brannmurinnstillinger som kan blokkere ICMP-pakker, noe som kan påvirke resultatene.
- Kombiner `traceroute6` med andre nettverksverktøy som `ping` for en mer omfattende feilsøking.