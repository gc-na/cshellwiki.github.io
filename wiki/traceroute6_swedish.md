# [Linux] Bash traceroute6 användning: Spåra IPv6-nätverksvägar

## Översikt
Kommandot `traceroute6` används för att spåra vägen som IPv6-paket tar genom ett nätverk. Det hjälper användare att diagnostisera nätverksproblem genom att visa varje hopp mellan källan och destinationen.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
traceroute6 [alternativ] [argument]
```

## Vanliga alternativ
- `-m <hops>`: Sätter det maximala antalet hopp som ska spåras.
- `-p <port>`: Anger portnumret som ska användas för att skicka paket.
- `-w <timeout>`: Sätter timeout för varje hopp i sekunder.
- `-n`: Använd IP-adresser istället för att försöka lösa domännamn.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `traceroute6`:

1. Spåra vägen till en IPv6-adress:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Spåra vägen med ett maximalt antal hopp på 15:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. Spåra vägen och använda en specifik port:
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. Spåra vägen utan att lösa domännamn:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

## Tips
- Använd `-n` alternativet för att snabba upp processen om du inte behöver domännamn.
- Kontrollera att din nätverkskonfiguration stödjer IPv6 innan du använder `traceroute6`.
- Tänk på att vissa nätverksbrandväggar kan blockera ICMP-paket, vilket kan påverka resultaten.