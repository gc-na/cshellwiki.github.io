# [Linux] Bash htop användning: Övervaka systemresurser i realtid

## Översikt
htop är ett interaktivt verktyg för att övervaka systemresurser i realtid. Det visar en dynamisk vy av systemprocesser, CPU-användning, minnesanvändning och andra viktiga systemstatistik. Till skillnad från det traditionella `top`-kommandot erbjuder htop en mer användarvänlig gränssnitt med färgkodning och möjlighet att navigera med piltangenterna.

## Användning
Den grundläggande syntaxen för htop är:

```bash
htop [alternativ] [argument]
```

## Vanliga alternativ
- `-h`, `--help`: Visa hjälpmeddelande.
- `-s`, `--sort`: Sortera processerna efter angiven kolumn.
- `-p`, `--pid`: Visa endast processer med angivna process-ID:n.
- `-u`, `--user`: Visa endast processer som tillhör en viss användare.

## Vanliga exempel
Här är några praktiska exempel på hur man använder htop:

1. **Starta htop**:
   ```bash
   htop
   ```

2. **Sortera processer efter CPU-användning**:
   ```bash
   htop -s PERCENT_CPU
   ```

3. **Visa processer för en specifik användare**:
   ```bash
   htop -u användarnamn
   ```

4. **Visa specifika processer med angivna PID**:
   ```bash
   htop -p 1234,5678
   ```

## Tips
- Använd piltangenterna för att navigera mellan processerna och tryck på `F9` för att avsluta en process.
- Tryck på `F2` för att öppna inställningar och anpassa visningen av htop.
- För att söka efter en specifik process, tryck på `F3` och skriv namnet på processen.
- Kom ihåg att htop kräver root-privilegier för att visa alla processer, så kör det med `sudo` om det behövs.