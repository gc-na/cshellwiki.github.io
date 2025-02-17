# [Linux] Bash traceroute användning: Spåra nätverksvägar

## Översikt
Kommandot `traceroute` används för att spåra vägen som datapaket tar från en dator till en specifik destination på nätverket. Det visar varje hopp mellan din dator och måldatorn, vilket kan hjälpa till att identifiera nätverksproblem.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
traceroute [alternativ] [mål]
```

## Vanliga alternativ
- `-m <hopp>`: Anger det maximala antalet hopp som ska spåras.
- `-n`: Visar IP-adresser istället för att försöka lösa domännamn.
- `-w <sekunder>`: Anger tidsgränsen för att vänta på ett svar från varje hopp.
- `-p <port>`: Anger portnumret som ska användas för att skicka paket.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `traceroute`:

1. Spåra vägen till en webbplats:
   ```bash
   traceroute www.example.com
   ```

2. Spåra vägen till en IP-adress med max 10 hopp:
   ```bash
   traceroute -m 10 192.168.1.1
   ```

3. Visa endast IP-adresser utan domännamn:
   ```bash
   traceroute -n www.example.com
   ```

4. Specifika portnummer för spårning:
   ```bash
   traceroute -p 80 www.example.com
   ```

## Tips
- Använd `-n` för att snabba upp processen om du inte behöver domännamn.
- Kontrollera att du har rätt behörigheter, eftersom vissa system kan blockera `traceroute`.
- Tänk på att vissa nätverksadministratörer kan blockera ICMP-paket, vilket kan påverka resultaten.