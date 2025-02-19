# [Linux] C Shell (csh) sqlite3 Verwendung: Datenbankverwaltung über die Kommandozeile

## Übersicht
Der Befehl `sqlite3` wird verwendet, um mit SQLite-Datenbanken über die Kommandozeile zu interagieren. Er ermöglicht das Erstellen, Bearbeiten und Abfragen von Datenbanken und ist ein leistungsstarkes Tool für die Datenbankverwaltung.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
sqlite3 [Optionen] [Argumente]
```

## Häufige Optionen
- `-help`: Zeigt eine Hilfe mit den verfügbaren Befehlen und Optionen an.
- `-version`: Gibt die aktuelle Version von SQLite aus.
- `-init FILE`: Führt die Befehle in der angegebenen Datei beim Start aus.
- `-batch`: Aktiviert den Batch-Modus, der die Eingabeaufforderung unterdrückt.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `sqlite3`:

1. **Eine neue Datenbank erstellen:**
   ```csh
   sqlite3 meine_datenbank.db
   ```

2. **Eine Tabelle erstellen:**
   ```csh
   sqlite3 meine_datenbank.db "CREATE TABLE benutzer (id INTEGER PRIMARY KEY, name TEXT);"
   ```

3. **Daten in die Tabelle einfügen:**
   ```csh
   sqlite3 meine_datenbank.db "INSERT INTO benutzer (name) VALUES ('Max Mustermann');"
   ```

4. **Daten abfragen:**
   ```csh
   sqlite3 meine_datenbank.db "SELECT * FROM benutzer;"
   ```

5. **Datenbank im Batch-Modus verwenden:**
   ```csh
   sqlite3 meine_datenbank.db < befehle.sql
   ```

## Tipps
- Verwenden Sie den Batch-Modus, wenn Sie mehrere Befehle aus einer Datei ausführen möchten, um die Effizienz zu steigern.
- Nutzen Sie die `-init` Option, um beim Starten der Datenbank automatisch Skripte auszuführen.
- Denken Sie daran, regelmäßig Backups Ihrer Datenbank zu erstellen, um Datenverlust zu vermeiden.