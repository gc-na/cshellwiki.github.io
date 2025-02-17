# [Linux] Bash nslookup användning: Hämta DNS-information

## Översikt
`nslookup` är ett kommandoradsverktyg som används för att fråga Domain Name System (DNS) för att få information om domännamn och IP-adresser. Det är användbart för att felsöka nätverksproblem och verifiera DNS-poster.

## Användning
Den grundläggande syntaxen för `nslookup` är:

```
nslookup [alternativ] [argument]
```

## Vanliga alternativ
- `-type=typ`: Anger vilken typ av DNS-post som ska hämtas (t.ex. A, AAAA, MX).
- `-timeout=sekunder`: Ställer in tidsgränsen för att vänta på svar.
- `-retry=antal`: Anger hur många gånger att försöka vid en begäran om den misslyckas.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `nslookup`:

1. Hämta IP-adressen för en domän:
   ```bash
   nslookup example.com
   ```

2. Hämta specifik typ av DNS-post, till exempel MX-poster:
   ```bash
   nslookup -type=MX example.com
   ```

3. Använda en specifik DNS-server för att göra en förfrågan:
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. Kontrollera AAAA-poster (IPv6-adresser):
   ```bash
   nslookup -type=AAAA example.com
   ```

## Tips
- Använd `nslookup` i kombination med andra nätverksverktyg som `ping` och `traceroute` för att få en mer komplett bild av nätverksproblem.
- Kom ihåg att `nslookup` kan ge olika resultat beroende på vilken DNS-server du använder.
- För mer avancerad användning, överväg att använda `dig`, som ger mer detaljerad information om DNS-poster.