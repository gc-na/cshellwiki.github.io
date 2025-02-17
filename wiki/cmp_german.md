# [Linux] Bash cmp Verwendung: Dateien vergleichen

## Übersicht
Der Befehl `cmp` wird verwendet, um zwei Dateien byteweise zu vergleichen. Er zeigt an, ob die Dateien identisch sind und gibt die Position der ersten Abweichung aus, falls Unterschiede vorhanden sind.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
cmp [Optionen] [Datei1] [Datei2]
```

## Häufige Optionen
- `-l`: Gibt die Unterschiede in Form von byteweisen Positionen und Werten aus.
- `-s`: Stille Ausgabe; gibt nur den Exit-Status zurück, ohne Ausgaben zu erzeugen.
- `-i OFFSET`: Beginnt den Vergleich bei der angegebenen Byte-Offset.
- `-n NUM`: Vergleicht nur die ersten NUM Bytes der Dateien.

## Häufige Beispiele
1. **Einfacher Vergleich zweier Dateien:**
   ```bash
   cmp datei1.txt datei2.txt
   ```

2. **Vergleich mit detaillierter Ausgabe der Unterschiede:**
   ```bash
   cmp -l datei1.txt datei2.txt
   ```

3. **Stille Überprüfung, ob zwei Dateien identisch sind:**
   ```bash
   cmp -s datei1.txt datei2.txt
   ```

4. **Vergleich ab einem bestimmten Offset:**
   ```bash
   cmp -i 10 datei1.txt datei2.txt
   ```

5. **Vergleich der ersten 100 Bytes zweier Dateien:**
   ```bash
   cmp -n 100 datei1.txt datei2.txt
   ```

## Tipps
- Verwenden Sie die Option `-s`, wenn Sie nur wissen möchten, ob die Dateien identisch sind, ohne die Unterschiede anzuzeigen.
- Nutzen Sie `-l`, um eine detaillierte Analyse der Unterschiede zu erhalten, was besonders hilfreich sein kann, wenn Sie an großen Dateien arbeiten.
- Achten Sie darauf, die Dateien in der richtigen Reihenfolge anzugeben, da `cmp` die Unterschiede nur in der ersten Datei im Vergleich zur zweiten anzeigt.