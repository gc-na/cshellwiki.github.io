# [Linux] Bash vid at: schemaläggning av kommandon

## Översikt
Kommandot `at` används för att schemalägga kommandon som ska köras vid en specifik tidpunkt i framtiden. Det är ett praktiskt verktyg för att automatisera uppgifter utan att behöva hålla terminalen öppen.

## Användning
Den grundläggande syntaxen för `at`-kommandot är:

```bash
at [alternativ] [argument]
```

## Vanliga alternativ
- `-f <fil>`: Anger en fil som innehåller kommandon som ska köras.
- `-m`: Skicka ett e-postmeddelande när kommandot har körts.
- `-q <kö>`: Anger vilken kö som ska användas för att schemalägga kommandot (t.ex. a, b, c).
- `-l`: Visar en lista över schemalagda jobb.

## Vanliga exempel
Här är några praktiska exempel på hur `at` kan användas:

1. Schemalägg ett kommando att köras vid en specifik tid:
   ```bash
   echo "backup.sh" | at 14:00
   ```

2. Schemalägg ett kommando att köras om 5 minuter:
   ```bash
   echo "echo 'Hello, World!'" | at now + 5 minutes
   ```

3. Använd en fil för att schemalägga flera kommandon:
   ```bash
   at -f myscript.sh 09:00
   ```

4. Lista alla schemalagda jobb:
   ```bash
   at -l
   ```

## Tips
- Kontrollera att `atd`-tjänsten är igång, eftersom den behövs för att `at` ska fungera korrekt.
- Använd `-m` alternativet om du vill få en bekräftelse via e-post när ditt jobb har körts.
- Tänk på att schemalagda jobb körs med den användares rättigheter som skapade dem, så se till att du har nödvändiga behörigheter för de kommandon du schemalägger.