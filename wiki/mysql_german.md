# [Linux] Bash mysql Verwendung: Datenbankverwaltung über die Kommandozeile

## Übersicht
Der `mysql` Befehl ist ein Kommandozeilen-Client für MySQL-Datenbanken. Er ermöglicht Benutzern, sich mit einer MySQL-Datenbank zu verbinden, SQL-Abfragen auszuführen und Daten zu verwalten. Mit `mysql` können Sie Daten abfragen, hinzufügen, aktualisieren und löschen.

## Verwendung
Die grundlegende Syntax des `mysql` Befehls lautet:

```bash
mysql [Optionen] [Argumente]
```

## Häufige Optionen
- `-u [Benutzername]`: Gibt den Benutzernamen an, mit dem Sie sich anmelden möchten.
- `-p`: Fordert zur Eingabe des Passworts auf.
- `-h [Host]`: Gibt den Hostnamen der MySQL-Datenbank an (Standard ist `localhost`).
- `-D [Datenbank]`: Gibt die Datenbank an, mit der Sie sich verbinden möchten.
- `--execute=[SQL-Befehl]`: Führt einen SQL-Befehl direkt aus und beendet die Sitzung.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `mysql` Befehls:

1. **Mit einer Datenbank verbinden:**
   ```bash
   mysql -u benutzername -p
   ```

2. **Mit einer bestimmten Datenbank verbinden:**
   ```bash
   mysql -u benutzername -p -D datenbankname
   ```

3. **Eine SQL-Abfrage ausführen:**
   ```bash
   mysql -u benutzername -p -D datenbankname --execute="SELECT * FROM tabelle;"
   ```

4. **Datenbank exportieren:**
   ```bash
   mysqldump -u benutzername -p datenbankname > backup.sql
   ```

5. **Datenbank importieren:**
   ```bash
   mysql -u benutzername -p datenbankname < backup.sql
   ```

## Tipps
- Verwenden Sie die Option `-h`, um sich mit einer Remote-Datenbank zu verbinden.
- Nutzen Sie `--execute`, um Skripte oder Befehle in einer einzigen Zeile auszuführen, ohne die MySQL-Sitzung zu starten.
- Achten Sie darauf, sensible Informationen wie Passwörter nicht in Skripten oder Protokollen zu speichern.
- Verwenden Sie `mysqldump`, um regelmäßige Backups Ihrer Datenbanken zu erstellen.