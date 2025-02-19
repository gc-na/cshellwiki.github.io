# [Linux] C Shell (csh) at: Befehle zeitgesteuert ausführen

## Übersicht
Der `at` Befehl wird verwendet, um Aufgaben zu einem bestimmten Zeitpunkt in der Zukunft auszuführen. Er ermöglicht es Benutzern, Befehle oder Skripte zu planen, die zu einem festgelegten Zeitpunkt automatisch ausgeführt werden.

## Verwendung
Die grundlegende Syntax des `at` Befehls lautet:

```
at [Optionen] [Zeit]
```

## Häufige Optionen
- `-f [Datei]`: Gibt eine Datei an, die die auszuführenden Befehle enthält.
- `-m`: Sendet eine E-Mail, wenn der Job abgeschlossen ist.
- `-q [Warteschlange]`: Gibt die Warteschlange an, in der der Job ausgeführt werden soll.
- `-l`: Listet die geplanten Jobs auf.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `at` Befehls:

1. **Einen Befehl in 10 Minuten ausführen**:
   ```bash
   echo "echo 'Hallo Welt'" | at now + 10 minutes
   ```

2. **Ein Skript zu einem bestimmten Zeitpunkt ausführen**:
   ```bash
   at 14:00 < /path/to/script.sh
   ```

3. **Einen Job für morgen um 8 Uhr planen**:
   ```bash
   echo "backup.sh" | at 08:00 tomorrow
   ```

4. **Einen Job mit einer E-Mail-Benachrichtigung planen**:
   ```bash
   echo "echo 'Job abgeschlossen'" | at -m now + 1 hour
   ```

5. **Geplante Jobs auflisten**:
   ```bash
   at -l
   ```

## Tipps
- Stellen Sie sicher, dass der `at` Daemon (`atd`) läuft, damit geplante Jobs ausgeführt werden können.
- Verwenden Sie die `-m` Option, um sicherzustellen, dass Sie eine Benachrichtigung erhalten, wenn der Job abgeschlossen ist.
- Planen Sie Jobs in einer Testumgebung, um sicherzustellen, dass sie wie erwartet funktionieren, bevor Sie sie in einer Produktionsumgebung einsetzen.