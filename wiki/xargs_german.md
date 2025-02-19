# [Linux] C Shell (csh) xargs Verwendung: Befehle mit Argumenten verarbeiten

## Übersicht
Der Befehl `xargs` wird verwendet, um Eingaben von Standard-Input (stdin) zu lesen und diese als Argumente an einen anderen Befehl zu übergeben. Dies ist besonders nützlich, wenn die Anzahl der Argumente zu groß ist, um sie direkt in der Kommandozeile zu übergeben.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
xargs [Optionen] [Argumente]
```

## Häufige Optionen
- `-n N`: Gibt an, dass maximal N Argumente pro Befehl übergeben werden.
- `-d DELIMITER`: Legt ein benutzerdefiniertes Trennzeichen für die Eingabe fest.
- `-p`: Fragt vor der Ausführung jedes Befehls um Bestätigung.
- `-0`: Erwartet, dass die Eingaben nullterminiert sind (nützlich mit `find -print0`).

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `xargs`:

1. **Dateien löschen**:
   ```bash
   find . -name "*.tmp" | xargs rm
   ```
   Dieser Befehl sucht nach allen `.tmp`-Dateien im aktuellen Verzeichnis und löscht sie.

2. **Dateien komprimieren**:
   ```bash
   find . -name "*.log" | xargs gzip
   ```
   Hier werden alle `.log`-Dateien gefunden und mit `gzip` komprimiert.

3. **Befehle mit begrenzter Argumentanzahl**:
   ```bash
   echo "file1 file2 file3 file4" | xargs -n 2 cp -t /backup/
   ```
   Dieser Befehl kopiert die Dateien in Gruppen von zwei in das Verzeichnis `/backup/`.

4. **Benutzerdefiniertes Trennzeichen**:
   ```bash
   echo "file1;file2;file3" | xargs -d ';' rm
   ```
   Hier wird das Semikolon als Trennzeichen verwendet, um die Dateien zu löschen.

## Tipps
- Verwenden Sie `-n` mit `xargs`, um die Anzahl der Argumente pro Befehl zu steuern und Überlauf zu vermeiden.
- Kombinieren Sie `xargs` mit `find` für leistungsstarke Dateimanipulationen.
- Nutzen Sie `-p`, um sicherzustellen, dass Sie keine unbeabsichtigten Änderungen vornehmen, insbesondere bei destruktiven Befehlen wie `rm`.