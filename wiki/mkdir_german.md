# [Linux] C Shell (csh) mkdir Verwendung: Verzeichnisse erstellen

## Übersicht
Der Befehl `mkdir` wird verwendet, um neue Verzeichnisse im Dateisystem zu erstellen. Mit diesem Befehl können Benutzer die Struktur ihrer Verzeichnisse organisieren und neue Ordner für ihre Dateien anlegen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
mkdir [optionen] [argumente]
```

## Häufige Optionen
- `-p`: Erstellt das Verzeichnis und alle übergeordneten Verzeichnisse, falls diese nicht existieren.
- `-m`: Setzt die Berechtigungen für das neu erstellte Verzeichnis, angegeben im octalen Format.
- `-v`: Gibt eine ausführliche Ausgabe aus, die anzeigt, welche Verzeichnisse erstellt wurden.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `mkdir`:

1. **Ein einfaches Verzeichnis erstellen:**
   ```csh
   mkdir meinVerzeichnis
   ```

2. **Mehrere Verzeichnisse gleichzeitig erstellen:**
   ```csh
   mkdir verzeichnis1 verzeichnis2 verzeichnis3
   ```

3. **Ein Verzeichnis mit übergeordneten Verzeichnissen erstellen:**
   ```csh
   mkdir -p /home/benutzer/neuerOrdner/unterordner
   ```

4. **Ein Verzeichnis mit bestimmten Berechtigungen erstellen:**
   ```csh
   mkdir -m 755 meinSicheresVerzeichnis
   ```

5. **Ausführliche Ausgabe beim Erstellen eines Verzeichnisses anzeigen:**
   ```csh
   mkdir -v meinNeuesVerzeichnis
   ```

## Tipps
- Verwenden Sie die `-p` Option, um sicherzustellen, dass alle erforderlichen übergeordneten Verzeichnisse erstellt werden, ohne dass Fehler auftreten.
- Überprüfen Sie die Berechtigungen des neuen Verzeichnisses mit dem Befehl `ls -l`, um sicherzustellen, dass sie Ihren Anforderungen entsprechen.
- Nutzen Sie die `-v` Option, um eine Bestätigung zu erhalten, dass das Verzeichnis erfolgreich erstellt wurde, besonders wenn Sie mehrere Verzeichnisse auf einmal erstellen.