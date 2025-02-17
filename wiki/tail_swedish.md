# [Linux] Bash tail användning: Visa de senaste raderna i en fil

## Översikt
`tail` är ett Bash-kommando som används för att visa de senaste raderna i en fil. Det är särskilt användbart för att övervaka loggfiler eller andra filer där nya data kontinuerligt läggs till.

## Användning
Den grundläggande syntaxen för `tail`-kommandot är:

```bash
tail [alternativ] [argument]
```

## Vanliga alternativ
- `-n [antal]`: Visa de senaste [antal] raderna från filen.
- `-f`: Följ filen i realtid, vilket innebär att nya rader visas automatiskt när de läggs till.
- `-c [antal]`: Visa de senaste [antal] byte från filen.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `tail`:

1. Visa de senaste 10 raderna i en fil:
   ```bash
   tail filnamn.txt
   ```

2. Visa de senaste 20 raderna i en fil:
   ```bash
   tail -n 20 filnamn.txt
   ```

3. Följ en loggfil i realtid:
   ```bash
   tail -f loggfil.log
   ```

4. Visa de senaste 50 byte från en fil:
   ```bash
   tail -c 50 filnamn.txt
   ```

## Tips
- Använd `tail -f` för att övervaka loggfiler i realtid, vilket är användbart för felsökning.
- Kombinera `tail` med andra kommandon som `grep` för att filtrera specifika rader. Till exempel:
  ```bash
  tail -f loggfil.log | grep "fel"
  ```
- Om du vill se de senaste raderna från flera filer kan du ange flera filnamn:
  ```bash
  tail fil1.txt fil2.txt
  ```