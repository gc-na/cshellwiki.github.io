# [Linux] Bash tcpdump användning: Fånga nätverkstrafik

## Översikt
Tcpdump är ett kraftfullt kommandoradsverktyg för att fånga och analysera nätverkstrafik. Det används ofta av systemadministratörer och nätverksanalytiker för att felsöka nätverksproblem och övervaka trafik.

## Användning
Den grundläggande syntaxen för tcpdump är:

```bash
tcpdump [alternativ] [argument]
```

## Vanliga alternativ
- `-i <interface>`: Specificera nätverksgränssnittet att lyssna på.
- `-n`: Visa IP-adresser istället för att översätta dem till värdnamn.
- `-v`: Visa mer detaljerad information om varje paket.
- `-c <antal>`: Avsluta efter att ha fångat ett visst antal paket.
- `-w <filnamn>`: Spara fångad trafik till en fil för senare analys.
- `-r <filnamn>`: Läs in och analysera en tidigare fångad trafikfil.

## Vanliga exempel
Här är några praktiska exempel på hur man använder tcpdump:

1. Fånga trafik på ett specifikt nätverksgränssnitt:
   ```bash
   tcpdump -i eth0
   ```

2. Fånga trafik utan att översätta IP-adresser:
   ```bash
   tcpdump -i eth0 -n
   ```

3. Fånga ett visst antal paket:
   ```bash
   tcpdump -i eth0 -c 10
   ```

4. Spara fångad trafik till en fil:
   ```bash
   tcpdump -i eth0 -w trafik.pcap
   ```

5. Läs in och analysera en tidigare fångad trafikfil:
   ```bash
   tcpdump -r trafik.pcap
   ```

## Tips
- Använd `-v` eller `-vv` för att få mer detaljerad information om paketen.
- Kombinera alternativ för att skräddarsy din fångst, till exempel `tcpdump -i eth0 -n -c 100` för att fånga 100 paket utan namnöversättning.
- Var medveten om att tcpdump kan generera mycket data; använd filtreringsalternativ för att fokusera på specifik trafik.