# [Linux] Bash unexpand användning: Konvertera tabbar till mellanslag

## Översikt
Kommandot `unexpand` används för att konvertera tabbar i textfiler till mellanslag. Detta är användbart när du vill säkerställa att texten har en konsekvent formatering, särskilt när den ska visas i miljöer som inte hanterar tabbar på samma sätt.

## Användning
Den grundläggande syntaxen för kommandot `unexpand` är:

```bash
unexpand [alternativ] [argument]
```

## Vanliga alternativ
- `-t, --tabs=NUM` : Anger hur många mellanslag som ska användas istället för en tabb. Standardvärdet är 8.
- `-a, --all` : Konverterar alla tabbar till mellanslag, inte bara de som kan konverteras till ett specifikt antal mellanslag.
- `-h, --help` : Visar hjälpmeddelande för kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `unexpand`:

1. Konvertera tabbar till mellanslag med standardinställningar:
   ```bash
   unexpand fil.txt
   ```

2. Spara resultatet i en ny fil:
   ```bash
   unexpand fil.txt > ny_fil.txt
   ```

3. Använda ett specifikt antal mellanslag istället för tabbar:
   ```bash
   unexpand -t 4 fil.txt
   ```

4. Konvertera alla tabbar i en fil:
   ```bash
   unexpand -a fil.txt
   ```

## Tips
- Kontrollera alltid resultatet av `unexpand` genom att använda `cat -A` för att se tabbar och mellanslag tydligt.
- Använd `unexpand` tillsammans med `grep` för att filtrera ut specifika rader innan du konverterar dem.
- Om du ofta arbetar med tabbar och mellanslag, överväg att skapa en alias för `unexpand` med dina vanligaste alternativ för att spara tid.