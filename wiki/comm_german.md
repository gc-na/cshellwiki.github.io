# [Linux] Bash comm-Befehl: Vergleiche zwei sortierte Dateien

## Übersicht
Der `comm`-Befehl wird verwendet, um zwei sortierte Dateien zeilenweise zu vergleichen. Er zeigt die Unterschiede und Übereinstimmungen zwischen den beiden Dateien an, was ihn nützlich für die Analyse von Textdateien macht.

## Verwendung
Die grundlegende Syntax des `comm`-Befehls lautet:

```bash
comm [Optionen] [Datei1] [Datei2]
```

## Häufige Optionen
- `-1`: Unterdrückt die Ausgabe der Zeilen, die nur in Datei1 vorhanden sind.
- `-2`: Unterdrückt die Ausgabe der Zeilen, die nur in Datei2 vorhanden sind.
- `-3`: Unterdrückt die Ausgabe der Zeilen, die in beiden Dateien vorhanden sind.
- `-i`: Ignoriert die Groß- und Kleinschreibung bei der Vergleichung.
- `-d`: Zeigt nur die Zeilen an, die in beiden Dateien vorhanden sind.

## Häufige Beispiele

1. **Einfacher Vergleich von zwei Dateien:**
   ```bash
   comm datei1.txt datei2.txt
   ```

2. **Nur die Zeilen anzeigen, die in Datei1, aber nicht in Datei2 sind:**
   ```bash
   comm -13 datei1.txt datei2.txt
   ```

3. **Nur die Zeilen anzeigen, die in beiden Dateien vorhanden sind:**
   ```bash
   comm -12 datei1.txt datei2.txt
   ```

4. **Vergleich unter Berücksichtigung der Groß- und Kleinschreibung ignorieren:**
   ```bash
   comm -i datei1.txt datei2.txt
   ```

## Tipps
- Stellen Sie sicher, dass die Dateien, die Sie vergleichen möchten, vor der Verwendung des `comm`-Befehls sortiert sind. Sie können dies mit dem `sort`-Befehl erreichen.
- Verwenden Sie die Optionen `-1`, `-2` und `-3` zusammen, um gezielt nur die gewünschten Informationen anzuzeigen.
- Nutzen Sie die Ausgabe von `comm` in Kombination mit anderen Befehlen, wie `grep` oder `awk`, um komplexere Datenanalysen durchzuführen.