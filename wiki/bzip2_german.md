# [Linux] Bash bzip2 Verwendung: Dateien komprimieren

## Übersicht
Der Befehl `bzip2` wird verwendet, um Dateien zu komprimieren und den Speicherplatz zu reduzieren. Er nutzt den Burrows-Wheeler-Algorithmus und bietet eine hohe Kompressionsrate, ist jedoch in der Regel langsamer als andere Komprimierungswerkzeuge wie `gzip`.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
bzip2 [Optionen] [Argumente]
```

## Häufige Optionen
- `-d`, `--decompress`: Dekomprimiert eine komprimierte Datei.
- `-k`, `--keep`: Behalte die Originaldatei nach der Kompression.
- `-f`, `--force`: Überschreibt vorhandene Dateien ohne Nachfrage.
- `-v`, `--verbose`: Zeigt detaillierte Informationen über den Komprimierungsprozess an.
- `-z`, `--compress`: Komprimiert die Datei (Standardverhalten).

## Häufige Beispiele
- **Komprimieren einer Datei:**
  ```bash
  bzip2 datei.txt
  ```
  Dies erstellt eine komprimierte Datei namens `datei.txt.bz2`.

- **Dekomprimieren einer Datei:**
  ```bash
  bzip2 -d datei.txt.bz2
  ```
  Dies stellt die ursprüngliche Datei `datei.txt` wieder her.

- **Komprimieren und Originaldatei behalten:**
  ```bash
  bzip2 -k datei.txt
  ```
  Dies erstellt `datei.txt.bz2`, behält jedoch auch die Originaldatei `datei.txt`.

- **Komprimieren mehrerer Dateien:**
  ```bash
  bzip2 datei1.txt datei2.txt
  ```
  Dies komprimiert beide Dateien in `datei1.txt.bz2` und `datei2.txt.bz2`.

- **Detaillierte Ausgabe während der Kompression:**
  ```bash
  bzip2 -v datei.txt
  ```
  Dies zeigt Informationen über den Komprimierungsprozess an.

## Tipps
- Verwenden Sie die Option `-k`, wenn Sie die Originaldatei nicht verlieren möchten.
- Für große Dateien kann die Kompression einige Zeit in Anspruch nehmen; planen Sie dies entsprechend ein.
- Überprüfen Sie die Komprimierungsrate mit `ls -lh`, um den Platzbedarf vor und nach der Kompression zu vergleichen.