# [Linux] C Shell (csh) htop Verwendung: Systemüberwachung in Echtzeit

## Übersicht
Der Befehl `htop` ist ein interaktives Prozess-Viewer-Tool, das eine dynamische Ansicht der Systemressourcen und der laufenden Prozesse bietet. Im Gegensatz zu dem traditionellen `top`-Befehl bietet `htop` eine benutzerfreundlichere Oberfläche mit mehr Funktionen zur Prozessverwaltung.

## Verwendung
Die grundlegende Syntax des `htop`-Befehls lautet:

```bash
htop [Optionen] [Argumente]
```

## Häufige Optionen
- `-d <Sekunden>`: Setzt die Aktualisierungsrate in Sekunden.
- `-p <PID>`: Zeigt nur den Prozess mit der angegebenen Prozess-ID an.
- `-u <Benutzer>`: Filtert die Prozesse nach dem angegebenen Benutzer.
- `--help`: Zeigt eine Hilfeübersicht der Optionen an.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `htop`:

1. **Einfaches Starten von htop:**
   ```bash
   htop
   ```

2. **Aktualisierungsrate auf 2 Sekunden setzen:**
   ```bash
   htop -d 2
   ```

3. **Prozess mit spezifischer PID anzeigen:**
   ```bash
   htop -p 1234
   ```

4. **Prozesse eines bestimmten Benutzers filtern:**
   ```bash
   htop -u benutzername
   ```

## Tipps
- Nutzen Sie die Pfeiltasten, um durch die Liste der Prozesse zu navigieren.
- Drücken Sie `F9`, um einen Prozess zu beenden, und wählen Sie das entsprechende Signal aus.
- Verwenden Sie `F3`, um nach Prozessen zu suchen, und `F4`, um die Liste zu filtern.
- Passen Sie die Anzeige an, indem Sie `F2` drücken, um die Einstellungen zu öffnen.