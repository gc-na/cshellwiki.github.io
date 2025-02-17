# [Linux] Bash timedatectl Verwendung: Zeit- und Datumseinstellungen verwalten

## Übersicht
Der Befehl `timedatectl` wird verwendet, um die Zeit- und Datumseinstellungen eines Linux-Systems zu verwalten. Er ermöglicht das Anzeigen und Ändern von Systemzeit, Zeitzone und NTP (Network Time Protocol) Einstellungen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
timedatectl [Optionen] [Argumente]
```

## Häufige Optionen
- `status`: Zeigt den aktuellen Status von Zeit und Datum an.
- `set-time <Zeit>`: Setzt die Systemzeit auf die angegebene Zeit.
- `set-timezone <Zeitzone>`: Ändert die Zeitzone des Systems.
- `set-ntp <boolean>`: Aktiviert oder deaktiviert NTP-Synchronisation.

## Häufige Beispiele
- **Aktuellen Status anzeigen:**
  ```bash
  timedatectl status
  ```

- **Systemzeit auf einen bestimmten Wert setzen:**
  ```bash
  timedatectl set-time '2023-10-01 12:00:00'
  ```

- **Zeitzone auf 'Europe/Berlin' ändern:**
  ```bash
  timedatectl set-timezone Europe/Berlin
  ```

- **NTP-Synchronisation aktivieren:**
  ```bash
  timedatectl set-ntp true
  ```

## Tipps
- Überprüfen Sie regelmäßig den Status mit `timedatectl status`, um sicherzustellen, dass Ihr System die richtige Zeit hat.
- Verwenden Sie die richtige Zeitzone, um Zeitstempel und Protokolle korrekt zu interpretieren.
- Aktivieren Sie NTP, um sicherzustellen, dass Ihr System automatisch die aktuelle Zeit synchronisiert.