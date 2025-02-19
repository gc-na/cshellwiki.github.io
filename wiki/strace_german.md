# [Linux] C Shell (csh) strace Verwendung: Systemaufrufe und Signale verfolgen

## Übersicht
Der Befehl `strace` wird verwendet, um die Systemaufrufe und Signale eines Programms zu verfolgen. Dies ist besonders nützlich für das Debugging und das Verständnis, wie ein Programm mit dem Betriebssystem interagiert.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
strace [Optionen] [Argumente]
```

## Häufige Optionen
- `-e trace=SYSCALL`: Verfolgt nur die angegebenen Systemaufrufe.
- `-o DATEI`: Leitet die Ausgabe in die angegebene Datei um.
- `-p PID`: Verfolgt den Prozess mit der angegebenen Prozess-ID.
- `-c`: Gibt eine Zusammenfassung der Systemaufrufe und deren Häufigkeit aus.
- `-f`: Verfolgt auch Kindprozesse, die durch den überwachten Prozess erstellt werden.

## Häufige Beispiele

1. **Ein einfaches Programm verfolgen:**
   ```csh
   strace ls
   ```

2. **Die Ausgabe in eine Datei umleiten:**
   ```csh
   strace -o ausgabe.txt ls
   ```

3. **Verfolgen eines laufenden Prozesses:**
   ```csh
   strace -p 1234
   ```

4. **Nur bestimmte Systemaufrufe verfolgen:**
   ```csh
   strace -e trace=open,close ls
   ```

5. **Zusammenfassung der Systemaufrufe anzeigen:**
   ```csh
   strace -c ls
   ```

## Tipps
- Verwenden Sie die Option `-f`, wenn Sie auch die Systemaufrufe von Kindprozessen verfolgen möchten.
- Nutzen Sie die Umleitung der Ausgabe, um die Ergebnisse später zu analysieren, insbesondere bei umfangreichen Ausgaben.
- Sehen Sie sich die man-Seite (`man strace`) an, um eine vollständige Liste der Optionen und deren Erklärungen zu erhalten.