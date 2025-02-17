# [Linux] Bash strace Verwendung: Systemaufrufe und Signale verfolgen

## Übersicht
Der Befehl `strace` ist ein leistungsstarkes Werkzeug in Linux, das verwendet wird, um die Systemaufrufe und Signale eines Programms zu verfolgen. Es ermöglicht Entwicklern und Systemadministratoren, zu verstehen, wie ein Programm mit dem Betriebssystem interagiert, indem es die von einem Prozess durchgeführten Systemaufrufe aufzeichnet.

## Verwendung
Die grundlegende Syntax des `strace`-Befehls lautet:

```bash
strace [Optionen] [Argumente]
```

## Häufige Optionen
- `-e trace=SYSCALL`: Verfolgt nur bestimmte Systemaufrufe.
- `-p PID`: Verfolgt einen bereits laufenden Prozess mit der angegebenen Prozess-ID (PID).
- `-o DATEI`: Leitet die Ausgabe in eine Datei um, anstatt sie auf dem Bildschirm anzuzeigen.
- `-c`: Zeigt eine Zusammenfassung der Systemaufrufe und deren Zeiten an.
- `-f`: Verfolgt auch Kindprozesse, die von dem überwachten Prozess erstellt werden.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `strace`:

1. **Ein einfaches Programm verfolgen:**
   ```bash
   strace ls
   ```

2. **Verfolgen eines laufenden Prozesses:**
   ```bash
   strace -p 1234
   ```

3. **Ausgabe in eine Datei umleiten:**
   ```bash
   strace -o output.txt ls
   ```

4. **Nur bestimmte Systemaufrufe verfolgen:**
   ```bash
   strace -e trace=open,close ls
   ```

5. **Zusammenfassung der Systemaufrufe anzeigen:**
   ```bash
   strace -c ls
   ```

## Tipps
- Verwenden Sie `strace` mit Bedacht, da es die Leistung des überwachten Programms beeinträchtigen kann.
- Nutzen Sie die Option `-o`, um die Ausgabe zu speichern und später zu analysieren, besonders bei umfangreichen Ausgaben.
- Kombinieren Sie `strace` mit anderen Tools wie `grep`, um spezifische Informationen schneller zu finden.