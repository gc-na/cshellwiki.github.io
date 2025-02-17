# [Linux] Bash netstat användning: Visa nätverksanslutningar och statistik

## Översikt
`netstat` är ett kraftfullt verktyg som används för att visa nätverksanslutningar, routingtabeller, gränssnittstatistik och mycket mer. Det är ett viktigt verktyg för att övervaka nätverksaktivitet och felsöka nätverksproblem.

## Användning
Den grundläggande syntaxen för `netstat` är:

```
netstat [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visar alla anslutningar och lyssnande portar.
- `-t`: Visar TCP-anslutningar.
- `-u`: Visar UDP-anslutningar.
- `-n`: Visar adresser och portnummer i numerisk form istället för att försöka lösa dem till namn.
- `-l`: Visar endast lyssnande portar.
- `-p`: Visar process-ID och namn för varje anslutning.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `netstat`:

1. Visa alla aktiva anslutningar:
   ```bash
   netstat -a
   ```

2. Visa endast TCP-anslutningar:
   ```bash
   netstat -t
   ```

3. Visa lyssnande portar:
   ```bash
   netstat -l
   ```

4. Visa anslutningar med numeriska adresser:
   ```bash
   netstat -n
   ```

5. Visa anslutningar med processinformation:
   ```bash
   netstat -p
   ```

## Tips
- Använd `netstat` tillsammans med `grep` för att filtrera specifika anslutningar, till exempel:
  ```bash
  netstat -a | grep 80
  ```
- För att få en mer detaljerad bild av nätverksanvändningen, kombinera `netstat` med andra verktyg som `ss` eller `lsof`.
- Kom ihåg att köra `netstat` med sudo om du vill se information om alla processer, inte bara dina egna.