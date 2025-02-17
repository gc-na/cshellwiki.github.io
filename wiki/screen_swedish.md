# [Linux] Bash screen användning: Hantera terminalsessioner

## Översikt
Kommandot `screen` används för att skapa och hantera flera terminalsessioner inom en enda terminalfönster. Det gör det möjligt för användare att köra program i bakgrunden och återansluta till dem senare, vilket är särskilt användbart för långvariga processer eller fjärranslutningar.

## Användning
Den grundläggande syntaxen för kommandot `screen` är:

```bash
screen [alternativ] [argument]
```

## Vanliga alternativ
- `-S <namn>`: Ger sessionen ett specifikt namn för enklare identifiering.
- `-d -r`: Kopplar från en session som körs i bakgrunden och återansluter till den.
- `-list`: Visar en lista över aktiva sessioner.
- `-X <kommando>`: Skickar ett kommando till en specifik session.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `screen`:

1. Skapa en ny session:
   ```bash
   screen
   ```

2. Ge sessionen ett namn:
   ```bash
   screen -S min_session
   ```

3. Koppla från en session:
   Tryck på `Ctrl + A` följt av `D` för att koppla från sessionen.

4. Återansluta till en kopplad session:
   ```bash
   screen -r min_session
   ```

5. Lista aktiva sessioner:
   ```bash
   screen -list
   ```

6. Skicka ett kommando till en specifik session:
   ```bash
   screen -S min_session -X stuff "echo Hej världen\n"
   ```

## Tips
- Använd namngivna sessioner för att enkelt hålla reda på flera aktiva sessioner.
- Kom ihåg att koppla från sessioner istället för att stänga terminalfönstret för att bevara dina processer.
- Utforska `screen`-hjälpen med `man screen` för att lära dig mer om avancerade funktioner och alternativ.