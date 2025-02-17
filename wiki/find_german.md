# [Linux] Bash find Verwendung: Dateien suchen

## Übersicht
Der `find`-Befehl wird verwendet, um Dateien und Verzeichnisse in einem Verzeichnisbaum zu suchen. Er bietet eine leistungsstarke Möglichkeit, nach Dateien basierend auf verschiedenen Kriterien wie Namen, Typ, Größe und Änderungsdatum zu suchen.

## Verwendung
Die grundlegende Syntax des `find`-Befehls lautet:

```bash
find [Optionen] [Argumente]
```

## Häufige Optionen
- `-name <Muster>`: Sucht nach Dateien, deren Namen dem angegebenen Muster entsprechen.
- `-type <Typ>`: Filtert die Suche nach dem Dateityp (z.B. `f` für reguläre Dateien, `d` für Verzeichnisse).
- `-size <Größe>`: Sucht nach Dateien, die eine bestimmte Größe haben (z.B. `+100k` für mehr als 100 Kilobyte).
- `-mtime <Tage>`: Sucht nach Dateien, die in den letzten n Tagen geändert wurden.
- `-exec <Befehl> {} \;`: Führt einen Befehl für jede gefundene Datei aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `find`-Befehls:

- Suchen nach einer Datei mit dem Namen `example.txt` im aktuellen Verzeichnis und allen Unterverzeichnissen:

```bash
find . -name "example.txt"
```

- Suchen nach allen Verzeichnissen im aktuellen Verzeichnisbaum:

```bash
find . -type d
```

- Suchen nach Dateien, die größer als 1 Megabyte sind:

```bash
find . -size +1M
```

- Suchen nach Dateien, die in den letzten 7 Tagen geändert wurden:

```bash
find . -mtime -7
```

- Ausführen eines Befehls (z.B. `rm`) für alle `.log`-Dateien im aktuellen Verzeichnisbaum:

```bash
find . -name "*.log" -exec rm {} \;
```

## Tipps
- Verwenden Sie `-iname` anstelle von `-name`, um die Groß- und Kleinschreibung bei der Namenssuche zu ignorieren.
- Kombinieren Sie mehrere Optionen, um die Suche zu verfeinern (z.B. `find . -type f -size +1M -mtime -30`).
- Testen Sie Ihre Befehle zuerst mit `-print`, um zu sehen, welche Dateien gefunden werden, bevor Sie Aktionen wie `-exec` ausführen.