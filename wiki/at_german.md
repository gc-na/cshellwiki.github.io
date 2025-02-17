# [Linux] Bash bei at: Aufgaben zeitgesteuert ausführen

## Übersicht
Der `at`-Befehl in Bash wird verwendet, um Aufgaben zu einem bestimmten Zeitpunkt in der Zukunft auszuführen. Dies ist nützlich, wenn Sie einen Befehl oder ein Skript zu einem späteren Zeitpunkt planen möchten, ohne einen laufenden Prozess oder einen Cron-Job zu verwenden.

## Verwendung
Die grundlegende Syntax des `at`-Befehls lautet:

```bash
at [Optionen] [Zeit]
```

## Häufige Optionen
- `-f DATEI`: Führt die Befehle aus der angegebenen Datei aus.
- `-m`: Sendet eine E-Mail, wenn der Job abgeschlossen ist, auch wenn keine Ausgabe erzeugt wurde.
- `-q QUEUE`: Gibt die Warteschlange an, in der der Job ausgeführt werden soll.
- `-l`: Listet die geplanten Jobs auf.
- `-d JOB_ID`: Löscht den angegebenen Job.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `at`-Befehls:

1. **Einen Befehl in 5 Minuten ausführen:**
   ```bash
   echo "echo 'Hallo Welt'" | at now + 5 minutes
   ```

2. **Ein Skript zu einer bestimmten Uhrzeit ausführen:**
   ```bash
   at 14:00 <<< "/path/to/script.sh"
   ```

3. **Einen Befehl für den nächsten Tag um 8 Uhr planen:**
   ```bash
   echo "backup.sh" | at 08:00 tomorrow
   ```

4. **Einen Job aus einer Datei ausführen:**
   ```bash
   at -f /path/to/commands.txt now + 1 hour
   ```

5. **Geplante Jobs auflisten:**
   ```bash
   at -l
   ```

## Tipps
- Überprüfen Sie regelmäßig mit `at -l`, welche Jobs geplant sind, um sicherzustellen, dass Sie den Überblick behalten.
- Verwenden Sie die `-m`-Option, um Benachrichtigungen zu erhalten, wenn Ihre Jobs abgeschlossen sind.
- Stellen Sie sicher, dass die Zeiteingabe im richtigen Format erfolgt, um Missverständnisse zu vermeiden.