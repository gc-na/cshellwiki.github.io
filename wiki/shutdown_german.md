# [Linux] Bash shutdown Verwendung: System herunterfahren oder neu starten

## Übersicht
Der Befehl `shutdown` wird verwendet, um ein Linux-System sicher herunterzufahren oder neu zu starten. Er ermöglicht es Benutzern, das System zu einem bestimmten Zeitpunkt oder nach einer bestimmten Verzögerung auszuschalten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
shutdown [Optionen] [Zeit] [Nachricht]
```

## Häufige Optionen
- `-h`: Fährt das System herunter.
- `-r`: Startet das System neu.
- `-P`: Schaltet das System aus (Power off).
- `now`: Fährt das System sofort herunter.
- `+m`: Fährt das System nach m Minuten herunter (z.B. `+5` für 5 Minuten).
- `hh:mm`: Fährt das System um die angegebene Uhrzeit herunter (z.B. `22:00` für 22 Uhr).
- `-c`: Bricht einen laufenden Shutdown-Vorgang ab.

## Häufige Beispiele

1. **System sofort herunterfahren:**
   ```bash
   shutdown -h now
   ```

2. **System in 10 Minuten herunterfahren:**
   ```bash
   shutdown -h +10
   ```

3. **System um 23:00 Uhr neu starten:**
   ```bash
   shutdown -r 23:00
   ```

4. **Shutdown-Vorgang abbrechen:**
   ```bash
   shutdown -c
   ```

5. **Nachricht an alle Benutzer senden:**
   ```bash
   shutdown -h +5 "Das System wird in 5 Minuten heruntergefahren. Bitte speichern Sie Ihre Arbeit."
   ```

## Tipps
- Verwenden Sie den `-c`-Schalter, um einen Shutdown abzubrechen, falls Sie es sich anders überlegen.
- Informieren Sie andere Benutzer über geplante Shutdowns, indem Sie eine Nachricht mit dem Befehl senden.
- Testen Sie den Befehl in einer sicheren Umgebung, um sich mit den verschiedenen Optionen vertraut zu machen, bevor Sie ihn auf einem Produktionssystem verwenden.