# [Linux] Bash mkdir Verwendung: Verzeichnisse erstellen

## Übersicht
Der Befehl `mkdir` (make directory) wird verwendet, um neue Verzeichnisse im Dateisystem zu erstellen. Er ist ein grundlegendes Werkzeug in der Bash, das es Benutzern ermöglicht, die Struktur ihrer Dateien und Ordner zu organisieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
mkdir [Optionen] [Argumente]
```

## Häufige Optionen
- `-p`: Erstellt das Verzeichnis und alle übergeordneten Verzeichnisse, falls diese nicht existieren.
- `-v`: Gibt eine detaillierte Ausgabe aus, die anzeigt, welche Verzeichnisse erstellt wurden.
- `-m`: Setzt die Berechtigungen für das neu erstellte Verzeichnis.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `mkdir`:

1. **Ein einfaches Verzeichnis erstellen:**
   ```bash
   mkdir meinVerzeichnis
   ```

2. **Mehrere Verzeichnisse gleichzeitig erstellen:**
   ```bash
   mkdir verzeichnis1 verzeichnis2 verzeichnis3
   ```

3. **Ein Verzeichnis und alle übergeordneten Verzeichnisse erstellen:**
   ```bash
   mkdir -p /home/benutzer/neuerOrdner/unterordner
   ```

4. **Ein Verzeichnis mit spezifischen Berechtigungen erstellen:**
   ```bash
   mkdir -m 755 meinSicheresVerzeichnis
   ```

5. **Detaillierte Ausgabe beim Erstellen eines Verzeichnisses:**
   ```bash
   mkdir -v meinNeuesVerzeichnis
   ```

## Tipps
- Verwenden Sie die `-p` Option, um sicherzustellen, dass alle erforderlichen übergeordneten Verzeichnisse erstellt werden, ohne dass Fehler auftreten.
- Überprüfen Sie die Berechtigungen des Verzeichnisses mit `ls -l`, um sicherzustellen, dass sie Ihren Anforderungen entsprechen.
- Nutzen Sie die `-v` Option, um eine Bestätigung zu erhalten, dass das Verzeichnis erfolgreich erstellt wurde, besonders wenn Sie mehrere Verzeichnisse gleichzeitig erstellen.