# [Linux] Bash sqlite3 gebruik: Interactieve databasebeheer

## Overzicht
De `sqlite3` opdracht is een commandoregelinterface voor het SQLite-databasebeheersysteem. Het stelt gebruikers in staat om databases te maken, te bewerken en te doorzoeken met behulp van SQL-commando's.

## Gebruik
De basis syntaxis van de `sqlite3` opdracht is als volgt:

```bash
sqlite3 [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-help`: Toont een lijst met beschikbare opties en hun beschrijvingen.
- `-version`: Geeft de versie van SQLite weer.
- `-init <bestand>`: Voert een SQL-script uit bij het starten van de sqlite3-shell.
- `-batch`: Voert de opdrachten uit zonder interactieve prompts.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `sqlite3` opdracht:

1. **Een nieuwe database maken:**
   ```bash
   sqlite3 mijn_database.db
   ```

2. **Een tabel aanmaken:**
   ```bash
   sqlite3 mijn_database.db "CREATE TABLE gebruikers (id INTEGER PRIMARY KEY, naam TEXT);"
   ```

3. **Gegevens invoegen:**
   ```bash
   sqlite3 mijn_database.db "INSERT INTO gebruikers (naam) VALUES ('Jan');"
   ```

4. **Gegevens opvragen:**
   ```bash
   sqlite3 mijn_database.db "SELECT * FROM gebruikers;"
   ```

5. **Een SQL-script uitvoeren:**
   ```bash
   sqlite3 mijn_database.db < script.sql
   ```

## Tips
- Zorg ervoor dat je regelmatig een back-up maakt van je databases om gegevensverlies te voorkomen.
- Gebruik de `-init` optie om automatisch een script uit te voeren bij het starten van sqlite3 voor repetitieve taken.
- Maak gebruik van de `-batch` optie wanneer je scripts uitvoert om te voorkomen dat je handmatig bevestigingen moet geven.