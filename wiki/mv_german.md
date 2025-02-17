# [Linux] Bash mv Verwendung: Dateien und Verzeichnisse verschieben oder umbenennen

## Übersicht
Der `mv`-Befehl in Bash wird verwendet, um Dateien und Verzeichnisse zu verschieben oder umzubenennen. Er ist ein grundlegendes Werkzeug für die Dateiverwaltung in Unix-ähnlichen Betriebssystemen.

## Verwendung
Die grundlegende Syntax des `mv`-Befehls lautet:

```bash
mv [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
- `-i`: Fragt vor dem Überschreiben von Dateien nach.
- `-u`: Verschiebt nur, wenn die Quelldatei neuer ist als die Zieldatei oder wenn die Zieldatei nicht existiert.
- `-v`: Zeigt die ausgeführten Aktionen an (verbose).
- `-n`: Verhindert das Überschreiben von Dateien.

## Häufige Beispiele

1. **Datei verschieben:**
   Um eine Datei von einem Verzeichnis in ein anderes zu verschieben:
   ```bash
   mv /pfad/zur/datei.txt /neuer/pfad/datei.txt
   ```

2. **Datei umbenennen:**
   Um eine Datei im selben Verzeichnis umzubenennen:
   ```bash
   mv alte_datei.txt neue_datei.txt
   ```

3. **Verzeichnis verschieben:**
   Um ein ganzes Verzeichnis zu verschieben:
   ```bash
   mv /pfad/zum/verzeichnis /neuer/pfad/
   ```

4. **Mit Bestätigung vor dem Überschreiben:**
   Um eine Datei zu verschieben und vor dem Überschreiben zu fragen:
   ```bash
   mv -i /pfad/zur/datei.txt /neuer/pfad/datei.txt
   ```

5. **Nur neuere Dateien verschieben:**
   Um nur neuere Dateien zu verschieben:
   ```bash
   mv -u /pfad/zur/datei.txt /neuer/pfad/datei.txt
   ```

## Tipps
- Verwenden Sie die `-i`-Option, um versehentliches Überschreiben zu vermeiden.
- Nutzen Sie die `-v`-Option, um eine Rückmeldung über die durchgeführten Aktionen zu erhalten.
- Seien Sie vorsichtig beim Verschieben von Verzeichnissen, da dies alle darin enthaltenen Dateien und Unterverzeichnisse beeinflusst.