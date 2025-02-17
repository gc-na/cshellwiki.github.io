# [Linux] Bash last användning: Visa senaste inloggningar

## Översikt
Kommandot `last` används för att visa en lista över de senaste användarinloggningarna på systemet. Det hämtar information från loggfiler och ger en översikt över när och var användare har loggat in och ut.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
last [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visa den fullständiga värdnamnet för varje användare.
- `-n [antal]`: Ange hur många poster som ska visas. Om inget antal anges visas alla.
- `-x`: Visa även systemstart och avstängningar.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `last`:

1. Visa de senaste inloggningarna:
   ```bash
   last
   ```

2. Visa de senaste 5 inloggningarna:
   ```bash
   last -n 5
   ```

3. Visa inloggningar med fullständiga värdnamn:
   ```bash
   last -a
   ```

4. Visa inloggningar och systemstart/avstängningar:
   ```bash
   last -x
   ```

5. Visa inloggningar för en specifik användare:
   ```bash
   last användarnamn
   ```

## Tips
- Använd `last -n 10` för att snabbt få en översikt över de senaste 10 inloggningarna.
- Kombinera `last` med `grep` för att filtrera specifika användare eller mönster.
- Kontrollera loggfilerna i `/var/log/wtmp` för mer detaljerad information om inloggningar.