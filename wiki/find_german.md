# [Linux] C Shell (csh) find Verwendung: Dateinamen finden

## Übersicht
Der `find`-Befehl wird verwendet, um Dateien und Verzeichnisse in einem Verzeichnisbaum zu suchen. Er ermöglicht es Benutzern, nach bestimmten Kriterien wie Namen, Typ, Größe und Änderungsdatum zu filtern.

## Verwendung
Die grundlegende Syntax des `find`-Befehls lautet:

```csh
find [Optionen] [Argumente]
```

## Häufige Optionen
- `-name`: Sucht nach Dateien mit einem bestimmten Namen.
- `-type`: Filtert nach Dateitypen (z.B. `f` für reguläre Dateien, `d` für Verzeichnisse).
- `-size`: Sucht nach Dateien einer bestimmten Größe.
- `-mtime`: Sucht nach Dateien, die in den letzten n Tagen geändert wurden.
- `-exec`: Führt einen Befehl für jede gefundene Datei aus.

## Häufige Beispiele
- Suchen nach einer Datei mit dem Namen "beispiel.txt" im aktuellen Verzeichnis und Unterverzeichnissen:

```csh
find . -name "beispiel.txt"
```

- Suchen nach allen Verzeichnissen im aktuellen Verzeichnisbaum:

```csh
find . -type d
```

- Suchen nach Dateien, die größer als 1 MB sind:

```csh
find . -size +1M
```

- Suchen nach Dateien, die in den letzten 7 Tagen geändert wurden:

```csh
find . -mtime -7
```

- Ausführen eines Befehls auf jeder gefundenen Datei, z.B. das Löschen von Dateien mit der Endung ".tmp":

```csh
find . -name "*.tmp" -exec rm {} \;
```

## Tipps
- Verwenden Sie `-iname` anstelle von `-name`, um die Suche nicht zwischen Groß- und Kleinschreibung zu unterscheiden.
- Kombinieren Sie mehrere Optionen, um die Suche zu verfeinern, z.B. `find . -type f -size +1M -mtime -30`.
- Testen Sie Ihre `find`-Befehle zuerst ohne `-exec`, um sicherzustellen, dass Sie die richtigen Dateien finden, bevor Sie Aktionen darauf ausführen.