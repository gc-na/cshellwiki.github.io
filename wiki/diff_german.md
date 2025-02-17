# [Linux] Bash diff Verwendung: Unterschiede zwischen Dateien anzeigen

## Übersicht
Der `diff`-Befehl wird verwendet, um Unterschiede zwischen zwei Dateien oder Verzeichnissen zu vergleichen. Er zeigt an, welche Zeilen in einer Datei hinzugefügt, entfernt oder geändert wurden, was besonders nützlich ist, um Änderungen im Code oder Text zu verfolgen.

## Verwendung
Die grundlegende Syntax des `diff`-Befehls lautet:

```bash
diff [Optionen] [Argumente]
```

## Häufige Optionen
- `-u`: Zeigt die Unterschiede im Unified-Format an, das einfacher zu lesen ist.
- `-c`: Gibt die Unterschiede im kontextuellen Format aus.
- `-i`: Ignoriert Groß- und Kleinschreibung bei der Vergleichung.
- `-w`: Ignoriert Leerzeichen und Tabulatoren.
- `-r`: Vergleicht Verzeichnisse rekursiv.

## Häufige Beispiele

1. **Einfacher Vergleich zweier Dateien:**
   ```bash
   diff datei1.txt datei2.txt
   ```

2. **Vergleich im Unified-Format:**
   ```bash
   diff -u datei1.txt datei2.txt
   ```

3. **Vergleich von Verzeichnissen:**
   ```bash
   diff -r verzeichnis1/ verzeichnis2/
   ```

4. **Ignorieren von Leerzeichen:**
   ```bash
   diff -w datei1.txt datei2.txt
   ```

5. **Vergleich mit kontextuellem Format:**
   ```bash
   diff -c datei1.txt datei2.txt
   ```

## Tipps
- Verwenden Sie die Option `-u`, um die Ausgabe leserlicher zu gestalten, insbesondere wenn Sie Änderungen in Code-Dateien überprüfen.
- Wenn Sie regelmäßig mit Versionskontrollsystemen arbeiten, können Sie `diff` verwenden, um Änderungen zwischen verschiedenen Versionen von Dateien zu vergleichen.
- Nutzen Sie die Option `-r`, um schnell Unterschiede zwischen zwei Verzeichnissen zu erkennen, was bei der Arbeit mit Projekten hilfreich ist.