# [Linux] C Shell (csh) cmp Verwendung: Vergleicht zwei Dateien byteweise

## Übersicht
Der `cmp` Befehl wird verwendet, um zwei Dateien byteweise zu vergleichen. Er zeigt an, ob die Dateien identisch sind oder an welcher Stelle sie sich unterscheiden.

## Verwendung
Die grundlegende Syntax des `cmp` Befehls lautet:

```csh
cmp [Optionen] [Datei1] [Datei2]
```

## Häufige Optionen
- `-l`: Gibt die Unterschiede in Form von byte-Offset und den unterschiedlichen Bytes aus.
- `-s`: Stille Ausgabe; gibt nur den Rückgabewert zurück, ohne Unterschiede anzuzeigen.
- `-i`: Ignoriert die ersten N Bytes der Dateien.

## Häufige Beispiele

1. **Einfacher Vergleich zweier Dateien:**
   ```csh
   cmp datei1.txt datei2.txt
   ```

2. **Vergleich mit detaillierter Ausgabe der Unterschiede:**
   ```csh
   cmp -l datei1.txt datei2.txt
   ```

3. **Stille Ausgabe, nur Rückgabewert:**
   ```csh
   cmp -s datei1.txt datei2.txt
   ```

4. **Ignorieren der ersten 10 Bytes:**
   ```csh
   cmp -i 10 datei1.txt datei2.txt
   ```

## Tipps
- Verwenden Sie die `-s` Option, wenn Sie nur wissen möchten, ob die Dateien unterschiedlich sind, ohne die Unterschiede anzuzeigen.
- Nutzen Sie die `-l` Option, um eine detaillierte Analyse der Unterschiede zu erhalten, besonders nützlich bei großen Dateien.
- Überprüfen Sie die Rückgabewerte von `cmp`, um festzustellen, ob die Dateien identisch sind (Rückgabewert 0), unterschiedlich (Rückgabewert 1) oder wenn eine der Dateien nicht existiert (Rückgabewert 2).