# [Linux] C Shell (csh) comm-Befehl: Vergleicht zwei sortierte Dateien

## Übersicht
Der `comm`-Befehl wird verwendet, um zwei sortierte Dateien zu vergleichen und die Unterschiede sowie die gemeinsamen Zeilen anzuzeigen. Dieser Befehl ist nützlich, um schnell die Unterschiede zwischen zwei Textdateien zu erkennen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
comm [Optionen] [Argumente]
```

## Häufige Optionen
- `-1`: Unterdrückt die Ausgabe der Zeilen, die nur in der ersten Datei vorhanden sind.
- `-2`: Unterdrückt die Ausgabe der Zeilen, die nur in der zweiten Datei vorhanden sind.
- `-3`: Unterdrückt die Ausgabe der Zeilen, die in beiden Dateien vorhanden sind.
- `-i`: Ignoriert Groß- und Kleinschreibung beim Vergleich.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `comm`-Befehls:

1. **Vergleich von zwei Dateien:**
   ```csh
   comm datei1.txt datei2.txt
   ```

2. **Nur die Zeilen anzeigen, die in der zweiten Datei vorhanden sind:**
   ```csh
   comm -13 datei1.txt datei2.txt
   ```

3. **Gemeinsame Zeilen zwischen zwei Dateien anzeigen:**
   ```csh
   comm -12 datei1.txt datei2.txt
   ```

4. **Vergleich unter Ignorierung der Groß- und Kleinschreibung:**
   ```csh
   comm -i datei1.txt datei2.txt
   ```

## Tipps
- Stellen Sie sicher, dass die Dateien, die Sie vergleichen möchten, vor der Verwendung des `comm`-Befehls sortiert sind, da dieser Befehl nur mit sortierten Dateien korrekt funktioniert.
- Verwenden Sie die Optionen `-1`, `-2` und `-3`, um die Ausgabe nach Ihren Bedürfnissen anzupassen und nur die relevanten Informationen anzuzeigen.
- Nutzen Sie den `sort`-Befehl, um Ihre Dateien vor dem Vergleich zu sortieren, falls sie noch nicht sortiert sind.