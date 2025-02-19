# [Linux] C Shell (csh) sqlite3 Gebruik: Interactieve databasebeheer

## Overzicht
De `sqlite3` opdracht is een commandoregelprogramma dat wordt gebruikt om SQLite-databases te beheren. Het stelt gebruikers in staat om SQL-opdrachten uit te voeren, databases te maken, te bewerken en gegevens op te vragen.

## Gebruik
De basis syntaxis van de `sqlite3` opdracht is als volgt:

```csh
sqlite3 [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-help`: Toont een lijst met beschikbare opties en hun beschrijvingen.
- `-version`: Geeft de versie van SQLite weer.
- `-init <bestand>`: Voert een SQL-script uit bij het opstarten van de database.
- `-batch`: Voert opdrachten uit zonder interactieve prompts.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `sqlite3`:

1. **Een nieuwe database maken:**
   ```csh
   sqlite3 mijn_database.db
   ```

2. **Een tabel maken:**
   ```csh
   sqlite3 mijn_database.db "CREATE TABLE gebruikers (id INTEGER PRIMARY KEY, naam TEXT);"
   ```

3. **Gegevens invoegen:**
   ```csh
   sqlite3 mijn_database.db "INSERT INTO gebruikers (naam) VALUES ('Jan');"
   ```

4. **Gegevens opvragen:**
   ```csh
   sqlite3 mijn_database.db "SELECT * FROM gebruikers;"
   ```

5. **Een SQL-script uitvoeren:**
   ```csh
   sqlite3 mijn_database.db < script.sql
   ```

## Tips
- Gebruik de `-init` optie om een SQL-script automatisch uit te voeren bij het starten van de database.
- Maak regelmatig back-ups van uw databases om gegevensverlies te voorkomen.
- Experimenteer met de interactieve modus door simpelweg `sqlite3 mijn_database.db` in te voeren en SQL-opdrachten direct in te voeren.