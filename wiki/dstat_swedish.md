# [Linux] Bash dstat användning: övervaka systemresurser i realtid

## Översikt
Dstat är ett kraftfullt verktyg för att övervaka systemresurser i realtid. Det kombinerar funktionaliteten hos flera andra verktyg som vmstat, iostat och netstat, vilket gör det möjligt att få en omfattande översikt över systemets prestanda och resursanvändning.

## Användning
Den grundläggande syntaxen för dstat är:

```bash
dstat [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Visa CPU-användning.
- `-d`: Visa diskaktivitet.
- `-n`: Visa nätverksaktivitet.
- `-m`: Visa minnesanvändning.
- `-p`: Visa processer.
- `--help`: Visa hjälpmeddelande med tillgängliga alternativ.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda dstat:

1. Visa CPU- och diskaktivitet:
   ```bash
   dstat -cd
   ```

2. Visa nätverks- och minnesanvändning:
   ```bash
   dstat -nm
   ```

3. Visa alla tillgängliga resurser:
   ```bash
   dstat -cdnm
   ```

4. Spara dstat-utdata till en fil för senare analys:
   ```bash
   dstat -cdnm > dstat_output.txt
   ```

5. Använda dstat med en specifik uppdateringsfrekvens (t.ex. var 2:a sekund):
   ```bash
   dstat -cd 2
   ```

## Tips
- Använd `dstat --help` för att snabbt få en översikt över alla tillgängliga alternativ.
- Kombinera olika alternativ för att få en mer detaljerad bild av systemets prestanda.
- Tänk på att dstat kan påverka systemets prestanda något, så använd det med försiktighet på produktionssystem.