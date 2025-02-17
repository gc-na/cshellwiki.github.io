# [Linux] Bash df användning: Visa diskutrymme

## Översikt
Kommandot `df` används för att visa tillgängligt och använt diskutrymme på filsystem. Det ger en översikt över hur mycket utrymme som används och hur mycket som är kvar på olika monterade filsystem.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
df [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Visar storlekar i ett lättläst format (t.ex. MB, GB).
- `-T`: Visar typ av filsystem för varje monterat filsystem.
- `-a`: Inkluderar även filsystem som har 0 byte ledigt utrymme.
- `-i`: Visar information om inodes istället för diskutrymme.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `df`:

1. Visa diskutrymme i ett lättläst format:
   ```bash
   df -h
   ```

2. Visa diskutrymme med filsystemtyp:
   ```bash
   df -T
   ```

3. Inkludera filsystem med 0 byte ledigt utrymme:
   ```bash
   df -a
   ```

4. Visa information om inodes:
   ```bash
   df -i
   ```

## Tips
- Använd `df -h` för att snabbt få en översikt över diskutrymmet i ett format som är lätt att förstå.
- Kombinera alternativ för att få mer detaljerad information, till exempel `df -hT` för att se både storlek och typ av filsystem.
- Kontrollera diskutrymme regelbundet för att undvika att fylla upp disken, vilket kan leda till systemproblem.