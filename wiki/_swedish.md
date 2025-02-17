# [Linux] Bash @ användning: Utför kommandon i bakgrunden

## Översikt
Kommandot `@` används för att köra processer i bakgrunden i Bash. Det gör att användaren kan fortsätta arbeta i terminalen medan kommandot körs utan att blockera terminalens användning.

## Användning
Den grundläggande syntaxen för kommandot är:

```
@ [alternativ] [argument]
```

## Vanliga alternativ
- `&` - Används för att köra ett kommando i bakgrunden.
- `disown` - Ta bort ett jobb från jobblistan så att det inte påverkas av terminalens stängning.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `@`:

1. Köra ett skript i bakgrunden:
   ```bash
   ./mitt_skript.sh &
   ```

2. Köra en långvarig process utan att blockera terminalen:
   ```bash
   sleep 60 &
   ```

3. Köra flera kommandon i bakgrunden:
   ```bash
   kommand1 & kommand2 &
   ```

4. Använda `disown` för att ta bort ett jobb från jobblistan:
   ```bash
   long_running_command &
   disown
   ```

## Tips
- Använd `jobs` för att se en lista över aktiva bakgrundsprocesser.
- Använd `fg` för att återföra en bakgrundsprocess till förgrunden om du behöver interagera med den.
- Kom ihåg att bakgrundsprocesser kan fortsätta köra även om du stänger terminalen, så använd `disown` om du vill att de ska fortsätta oberoende av terminalens status.