# [Linux] Bash chmod Verwendung: Dateiberechtigungen ändern

## Übersicht
Der `chmod`-Befehl in Bash wird verwendet, um die Berechtigungen von Dateien und Verzeichnissen zu ändern. Mit diesem Befehl können Benutzer festlegen, wer auf eine Datei zugreifen, sie lesen oder ändern kann.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
chmod [Optionen] [Berechtigungen] [Datei/Verzeichnis]
```

## Häufige Optionen
- `-R`: Ändert die Berechtigungen rekursiv für alle Dateien und Unterverzeichnisse.
- `-v`: Gibt eine ausführliche Ausgabe aus, die zeigt, welche Berechtigungen geändert wurden.
- `-c`: Gibt nur Änderungen aus, die tatsächlich vorgenommen wurden.

## Häufige Beispiele
1. **Berechtigungen für eine Datei auf 755 setzen:**
   ```bash
   chmod 755 meine_datei.txt
   ```
   Dies gibt dem Besitzer volle Berechtigungen und anderen Benutzern Lese- und Ausführungsrechte.

2. **Rekursiv Berechtigungen für ein Verzeichnis ändern:**
   ```bash
   chmod -R 700 mein_verzeichnis
   ```
   Dies gibt dem Besitzer volle Berechtigungen und anderen Benutzern keinen Zugriff auf das Verzeichnis und dessen Inhalt.

3. **Berechtigungen für eine Datei hinzufügen:**
   ```bash
   chmod +x skript.sh
   ```
   Dies fügt Ausführungsrechte für alle Benutzer zur Datei `skript.sh` hinzu.

4. **Berechtigungen für eine Datei entfernen:**
   ```bash
   chmod -r w meine_datei.txt
   ```
   Dies entfernt das Schreibrecht für alle Benutzer von `meine_datei.txt`.

## Tipps
- Verwenden Sie `chmod -v`, um zu sehen, welche Änderungen vorgenommen wurden, besonders bei vielen Dateien.
- Seien Sie vorsichtig mit rekursiven Änderungen, um unbeabsichtigte Berechtigungsänderungen zu vermeiden.
- Überprüfen Sie die aktuellen Berechtigungen mit `ls -l`, bevor Sie Änderungen vornehmen.