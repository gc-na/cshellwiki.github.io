# [Linux] Bash sqlite3 Verwendung: Interagieren mit SQLite-Datenbanken

## Übersicht
Der Befehl `sqlite3` wird verwendet, um mit SQLite-Datenbanken zu interagieren. Er ermöglicht das Erstellen, Abfragen, Aktualisieren und Löschen von Daten in einer SQLite-Datenbank über die Kommandozeile.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
sqlite3 [Optionen] [Datenbankdatei]
```

## Häufige Optionen
- `-init <Datei>`: Führt die SQL-Befehle in der angegebenen Datei beim Start aus.
- `-header`: Zeigt die Spaltenüberschriften in den Abfrageergebnissen an.
- `-csv`: Gibt die Ergebnisse im CSV-Format aus.
- `-batch`: Schaltet den interaktiven Modus aus und führt Befehle im Batch-Modus aus.
- `-version`: Zeigt die Version von SQLite an.

## Häufige Beispiele

### 1. Erstellen einer neuen Datenbank
```bash
sqlite3 meine_datenbank.db
```

### 2. Erstellen einer Tabelle
```bash
sqlite3 meine_datenbank.db "CREATE TABLE benutzer (id INTEGER PRIMARY KEY, name TEXT);"
```

### 3. Einfügen von Daten
```bash
sqlite3 meine_datenbank.db "INSERT INTO benutzer (name) VALUES ('Max Mustermann');"
```

### 4. Abfragen von Daten
```bash
sqlite3 meine_datenbank.db "SELECT * FROM benutzer;"
```

### 5. Exportieren von Abfrageergebnissen im CSV-Format
```bash
sqlite3 -header -csv meine_datenbank.db "SELECT * FROM benutzer;" > benutzer.csv
```

## Tipps
- Verwenden Sie die Option `-header`, um die Lesbarkeit der Abfrageergebnisse zu verbessern.
- Nutzen Sie die `-init`-Option, um häufig verwendete SQL-Befehle automatisch beim Start auszuführen.
- Speichern Sie Ihre SQL-Befehle in einer Datei und verwenden Sie den Batch-Modus, um mehrere Befehle auf einmal auszuführen.