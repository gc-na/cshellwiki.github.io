# [Linux] Bash nslookup brug: Forespørgsel af DNS-oplysninger

## Oversigt
`nslookup` er et kommandolinjeværktøj, der bruges til at forespørge Domain Name System (DNS) for at få oplysninger om domænenavne og IP-adresser. Det er nyttigt til fejlfinding af netværksproblemer og til at finde ud af, hvilken IP-adresse der svarer til et givet domænenavn.

## Brug
Den grundlæggende syntaks for `nslookup`-kommandoen er:

```bash
nslookup [muligheder] [argumenter]
```

## Almindelige muligheder
- `-type=TYPE`: Angiver hvilken type DNS-post, der skal forespørges (f.eks. A, AAAA, MX).
- `-timeout=SECONDS`: Angiver timeout for forespørgsler i sekunder.
- `-retry=NUMBER`: Angiver antallet af forsøg, der skal gøres, hvis der ikke modtages svar.
- `-debug`: Aktiverer fejlfinding for at vise detaljerede oplysninger om forespørgslen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `nslookup`:

1. Forespørgsel om en IP-adresse for et domæne:
   ```bash
   nslookup www.example.com
   ```

2. Forespørgsel om en specifik DNS-posttype (f.eks. MX):
   ```bash
   nslookup -type=MX example.com
   ```

3. Angivelse af en specifik DNS-server til forespørgslen:
   ```bash
   nslookup www.example.com 8.8.8.8
   ```

4. Brug af debug-tilstand for at få flere oplysninger:
   ```bash
   nslookup -debug www.example.com
   ```

## Tips
- Brug `nslookup` til hurtigt at kontrollere, om et domæne er korrekt konfigureret i DNS.
- Vær opmærksom på, at nogle DNS-servere kan have cache, hvilket kan påvirke resultaterne af dine forespørgsler.
- Overvej at bruge `dig`-kommandoen som et alternativ til `nslookup`, da den giver mere detaljerede oplysninger og er mere fleksibel.