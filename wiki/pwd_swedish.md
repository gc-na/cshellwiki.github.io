# [Linux] Bash pwd användning: Visar den aktuella katalogen

## Översikt
Kommandot `pwd` (print working directory) används för att visa den aktuella arbetskatalogen i terminalen. Det är ett enkelt men viktigt verktyg för att navigera i filsystemet.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
pwd [alternativ]
```

## Vanliga alternativ
- `-L`: Visar den logiska sökvägen till den aktuella katalogen, vilket kan inkludera symboliska länkar.
- `-P`: Visar den fysiska sökvägen till den aktuella katalogen, utan att följa symboliska länkar.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `pwd`:

1. Visa den aktuella katalogen:
   ```bash
   pwd
   ```

2. Visa den logiska sökvägen:
   ```bash
   pwd -L
   ```

3. Visa den fysiska sökvägen:
   ```bash
   pwd -P
   ```

## Tips
- Använd `pwd` ofta för att bekräfta din nuvarande plats i filsystemet, särskilt när du navigerar genom flera kataloger.
- Kombinera `pwd` med andra kommandon för att skapa skript som automatiskt kan logga eller hantera katalogvägar.
- Kom ihåg att `pwd` alltid ger dig den fullständiga sökvägen, vilket kan vara användbart för att undvika förvirring när du arbetar med flera terminalfönster.