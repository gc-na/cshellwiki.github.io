# [Linux] Bash cp Verwendung: Dateien und Verzeichnisse kopieren

## Übersicht
Der `cp`-Befehl in Bash wird verwendet, um Dateien und Verzeichnisse zu kopieren. Er ermöglicht es Benutzern, Daten von einem Ort zu einem anderen zu übertragen, während die Originaldateien unverändert bleiben.

## Verwendung
Die grundlegende Syntax des `cp`-Befehls lautet:

```bash
cp [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
- `-r`: Kopiert Verzeichnisse rekursiv.
- `-i`: Fragt vor dem Überschreiben von Dateien nach.
- `-u`: Kopiert nur, wenn die Quell-Datei neuer ist als die Ziel-Datei oder wenn die Ziel-Datei nicht existiert.
- `-v`: Zeigt die Fortschritte beim Kopieren an (verbose).
- `-a`: Archivmodus; kopiert Dateien und Verzeichnisse rekursiv und bewahrt die Dateiattribute.

## Häufige Beispiele
1. **Eine Datei kopieren:**
   ```bash
   cp datei.txt kopie_datei.txt
   ```

2. **Ein Verzeichnis rekursiv kopieren:**
   ```bash
   cp -r mein_verzeichnis/ kopie_verzeichnis/
   ```

3. **Datei mit Bestätigung vor dem Überschreiben kopieren:**
   ```bash
   cp -i datei.txt kopie_datei.txt
   ```

4. **Nur neuere Dateien kopieren:**
   ```bash
   cp -u datei.txt zielverzeichnis/
   ```

5. **Kopieren mit Fortschrittsanzeige:**
   ```bash
   cp -v datei.txt zielverzeichnis/
   ```

## Tipps
- Verwenden Sie die `-i`-Option, um versehentliches Überschreiben wichtiger Dateien zu vermeiden.
- Bei der Verwendung von `-r` für Verzeichnisse sollten Sie sicherstellen, dass Sie die korrekten Verzeichnisse angeben, um Datenverlust zu vermeiden.
- Nutzen Sie die `-a`-Option, wenn Sie eine vollständige Kopie eines Verzeichnisses mit allen Attributen und Berechtigungen benötigen.