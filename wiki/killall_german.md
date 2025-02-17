# [Linux] Bash killall Verwendung: Beenden von Prozessen

## Übersicht
Der Befehl `killall` wird verwendet, um Prozesse anhand ihres Namens zu beenden. Dies ist besonders nützlich, wenn mehrere Instanzen eines Programms laufen und Sie alle gleichzeitig schließen möchten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
killall [Optionen] [Argumente]
```

## Häufige Optionen
- `-u <Benutzer>`: Beendet nur die Prozesse, die von dem angegebenen Benutzer ausgeführt werden.
- `-i`: Fragt vor dem Beenden jedes Prozesses nach Bestätigung.
- `-q`: Unterdrückt die Ausgabe von Fehlermeldungen.
- `-s <Signal>`: Gibt das zu sendende Signal an (z.B. `SIGTERM`, `SIGKILL`).

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `killall`:

1. Alle Instanzen eines Programms beenden:
   ```bash
   killall firefox
   ```

2. Alle Prozesse eines bestimmten Benutzers beenden:
   ```bash
   killall -u benutzername
   ```

3. Vor dem Beenden nach Bestätigung fragen:
   ```bash
   killall -i gedit
   ```

4. Ein spezifisches Signal senden (z.B. SIGKILL):
   ```bash
   killall -s SIGKILL myprocess
   ```

5. Alle Prozesse mit unterdrückter Fehlermeldung beenden:
   ```bash
   killall -q myprocess
   ```

## Tipps
- Verwenden Sie `killall -i`, um sicherzustellen, dass Sie keine wichtigen Prozesse versehentlich beenden.
- Seien Sie vorsichtig mit `SIGKILL`, da es Prozesse sofort beendet, ohne ihnen die Möglichkeit zu geben, ihre Arbeit zu speichern.
- Überprüfen Sie mit `ps aux`, welche Prozesse gerade laufen, bevor Sie `killall` verwenden, um sicherzustellen, dass Sie die richtigen Prozesse beenden.