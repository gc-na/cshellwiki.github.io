# [Linux] Bash uname användning: Visa systeminformation

## Översikt
`uname` är ett kommandot som används för att visa systeminformation om operativsystemet och maskinvaran på en Unix-liknande plattform. Det kan ge detaljer som systemets namn, version och arkitektur.

## Användning
Den grundläggande syntaxen för `uname` är:

```bash
uname [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visar all tillgänglig systeminformation.
- `-s`: Visar namnet på kärnan.
- `-n`: Visar nätverksnamnet på värddatorn.
- `-r`: Visar kärnans versionsnummer.
- `-v`: Visar kärnans versionsinformation.
- `-m`: Visar maskinens hårdvaruarkitektur.
- `-p`: Visar processorarkitekturen (om tillgänglig).
- `-i`: Visar plattformens information (om tillgänglig).
- `-o`: Visar operativsystemets namn.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `uname`:

1. Visa all systeminformation:
   ```bash
   uname -a
   ```

2. Visa endast kärnans namn:
   ```bash
   uname -s
   ```

3. Visa kärnans versionsnummer:
   ```bash
   uname -r
   ```

4. Visa maskinens hårdvaruarkitektur:
   ```bash
   uname -m
   ```

5. Visa nätverksnamnet på värddatorn:
   ```bash
   uname -n
   ```

## Tips
- Använd `uname -a` för att få en snabb översikt över hela systemets information.
- Kombinera `uname` med andra kommandon, som `grep`, för att filtrera specifik information.
- Kontrollera att du har rättigheter att köra kommandot om du får några felmeddelanden.