# [Linux] Bash w användning: Visa inloggade användare och deras aktivitet

## Översikt
Kommandot `w` används för att visa information om inloggade användare och deras aktivitet på systemet. Det ger en översikt över vilka användare som är inloggade, deras inloggningstid, och vad de gör för tillfället.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
w [alternativ]
```

## Vanliga alternativ
- `-h`: Visa inte rubrikerna.
- `-s`: Visa en kortare version av utdata.
- `-u`: Visa användarens inloggningstid i en mer läsbar form.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `w`:

1. Visa alla inloggade användare:
   ```bash
   w
   ```

2. Visa inloggade användare utan rubriker:
   ```bash
   w -h
   ```

3. Visa en kortare version av utdata:
   ```bash
   w -s
   ```

4. Visa inloggningstider i en mer läsbar form:
   ```bash
   w -u
   ```

## Tips
- Använd `w` för att snabbt kontrollera systemets användartillstånd, särskilt på servrar med flera användare.
- Kombinera `w` med andra kommandon som `grep` för att filtrera ut specifika användare.
- Tänk på att `w` kan ge känslig information, så använd det med försiktighet på delade system.