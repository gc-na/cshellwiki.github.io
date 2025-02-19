# [Linux] C Shell (csh) diff Verwendung: Vergleiche Dateien und zeigt Unterschiede an

## Übersicht
Der `diff` Befehl wird verwendet, um Unterschiede zwischen zwei Dateien oder Verzeichnissen zu vergleichen. Er zeigt an, welche Zeilen in einer Datei hinzugefügt, entfernt oder geändert wurden, was besonders nützlich ist, um Änderungen im Code oder in Textdokumenten nachzuvollziehen.

## Verwendung
Die grundlegende Syntax des `diff` Befehls lautet:

```
diff [Optionen] [Argumente]
```

## Häufige Optionen
- `-u`: Zeigt die Unterschiede im Unified-Format an, das eine bessere Lesbarkeit bietet.
- `-c`: Gibt die Unterschiede im kontextuellen Format aus, das mehr Kontext um die Änderungen herum zeigt.
- `-i`: Ignoriert Groß- und Kleinschreibung bei der Vergleichung.
- `-w`: Ignoriert Leerzeichen und Tabulatoren.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `diff` Befehls:

1. **Einfacher Vergleich von zwei Dateien:**
   ```csh
   diff datei1.txt datei2.txt
   ```

2. **Vergleich im Unified-Format:**
   ```csh
   diff -u datei1.txt datei2.txt
   ```

3. **Vergleich mit ignorierten Groß- und Kleinschreibungen:**
   ```csh
   diff -i datei1.txt datei2.txt
   ```

4. **Vergleich von zwei Verzeichnissen:**
   ```csh
   diff -r verzeichnis1/ verzeichnis2/
   ```

5. **Ausgabe im kontextuellen Format:**
   ```csh
   diff -c datei1.txt datei2.txt
   ```

## Tipps
- Verwenden Sie die `-u` Option, um die Ausgabe leichter lesbar zu machen, insbesondere bei größeren Änderungen.
- Nutzen Sie die `-r` Option, um alle Dateien in zwei Verzeichnissen rekursiv zu vergleichen.
- Speichern Sie die Ausgabe von `diff` in einer Datei, um die Unterschiede später zu überprüfen:
  ```csh
  diff -u datei1.txt datei2.txt > unterschiede.txt
  ```