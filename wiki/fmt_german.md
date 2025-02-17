# [Linux] Bash fmt Verwendung: Textformatierung für lesbare Ausgaben

## Übersicht
Der `fmt`-Befehl wird verwendet, um Textdateien zu formatieren und leserfreundlich zu gestalten. Er passt die Breite der Zeilen an und entfernt überflüssige Leerzeichen, um den Text klarer und strukturierter darzustellen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
fmt [Optionen] [Datei]
```

## Häufige Optionen
- `-w, --width=N`: Setzt die maximale Breite der Zeilen auf N Zeichen.
- `-s, --split-only`: Teilt nur an Leerzeichen, ohne zusätzliche Zeilenumbrüche hinzuzufügen.
- `-u, --uniform`: Formatiert den Text gleichmäßig, sodass alle Zeilen die gleiche Länge haben.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `fmt`-Befehls:

### Beispiel 1: Standardformatierung
Um eine Textdatei namens `beispiel.txt` zu formatieren, verwenden Sie den folgenden Befehl:

```bash
fmt beispiel.txt
```

### Beispiel 2: Zeilenbreite anpassen
Um die Zeilenbreite auf 50 Zeichen zu setzen, verwenden Sie die `-w`-Option:

```bash
fmt -w 50 beispiel.txt
```

### Beispiel 3: Nur an Leerzeichen teilen
Um den Text nur an Leerzeichen zu teilen, ohne zusätzliche Zeilenumbrüche hinzuzufügen:

```bash
fmt -s beispiel.txt
```

### Beispiel 4: Einheitliche Formatierung
Um den Text gleichmäßig zu formatieren, sodass alle Zeilen die gleiche Länge haben:

```bash
fmt -u beispiel.txt
```

## Tipps
- Verwenden Sie die `-w`-Option, um sicherzustellen, dass Ihre Ausgaben in verschiedenen Umgebungen gut lesbar sind.
- Kombinieren Sie Optionen, um die Formatierung weiter anzupassen, z.B. `fmt -w 60 -s beispiel.txt`.
- Überprüfen Sie die Ausgabe, um sicherzustellen, dass der Text nach Ihren Wünschen formatiert ist, insbesondere bei langen Absätzen.