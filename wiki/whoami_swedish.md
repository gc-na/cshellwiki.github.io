# [Linux] Bash whoami användning: Visa det aktuella användarnamnet

## Översikt
Kommandot `whoami` används för att visa det aktuella användarnamnet för den inloggade användaren i terminalen. Det är ett enkelt och effektivt sätt att snabbt få information om vilken användare som för närvarande är aktiv.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
whoami [alternativ] [argument]
```

## Vanliga alternativ
- `--help`: Visar hjälpinformation om kommandot.
- `--version`: Visar versionen av `whoami`-kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `whoami`:

1. Visa det aktuella användarnamnet:
   ```bash
   whoami
   ```

2. Visa hjälpinformation:
   ```bash
   whoami --help
   ```

3. Visa versionen av `whoami`:
   ```bash
   whoami --version
   ```

## Tips
- Använd `whoami` för att snabbt bekräfta vilket användarnamn du är inloggad som, särskilt när du arbetar med flera användarkonton.
- Det kan vara användbart i skript för att kontrollera om skriptet körs med rätt användarbehörigheter.