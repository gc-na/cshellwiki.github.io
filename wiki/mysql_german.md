# [Linux] C Shell (csh) mysql Verwendung: Datenbankverwaltung über die Kommandozeile

## Übersicht
Der `mysql` Befehl ist ein Client-Programm, das es Benutzern ermöglicht, mit MySQL-Datenbanken über die Kommandozeile zu interagieren. Mit diesem Befehl können Sie SQL-Abfragen ausführen, Datenbanken erstellen, verwalten und abfragen.

## Verwendung
Die grundlegende Syntax des `mysql` Befehls lautet:

```bash
mysql [Optionen] [Argumente]
```

## Häufige Optionen
- `-u [Benutzername]`: Gibt den Benutzernamen an, mit dem Sie sich bei der Datenbank anmelden möchten.
- `-p`: Fordert zur Eingabe des Passworts auf.
- `-h [Host]`: Gibt den Hostnamen des MySQL-Servers an (Standard ist localhost).
- `-D [Datenbank]`: Wählt die Datenbank aus, mit der Sie arbeiten möchten.
- `--execute [SQL-Befehl]`: Führt einen SQL-Befehl direkt aus und beendet die Sitzung.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `mysql` Befehls:

1. **Anmelden bei MySQL:**
   ```bash
   mysql -u root -p
   ```

2. **Datenbank auswählen und eine Tabelle abfragen:**
   ```bash
   mysql -u benutzer -p -D meineDatenbank -e "SELECT * FROM meineTabelle;"
   ```

3. **Eine neue Datenbank erstellen:**
   ```bash
   mysql -u benutzer -p -e "CREATE DATABASE neueDatenbank;"
   ```

4. **Ein SQL-Skript aus einer Datei ausführen:**
   ```bash
   mysql -u benutzer -p -D meineDatenbank < meinSkript.sql
   ```

## Tipps
- Verwenden Sie die Option `-h`, um sich mit einem Remote-MySQL-Server zu verbinden.
- Nutzen Sie die `--execute` Option für schnelle Abfragen, ohne die MySQL-Shell zu betreten.
- Speichern Sie häufig verwendete Befehle in Skripten, um die Effizienz zu steigern.