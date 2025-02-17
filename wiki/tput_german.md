# [Linux] Bash tput Verwendung: Terminalsteuerung und -formatierung

## Übersicht
Der Befehl `tput` wird verwendet, um Terminalsteuerungs- und Formatierungsbefehle auszuführen. Er ermöglicht es Benutzern, die Anzeige im Terminal zu steuern, indem er Funktionen wie das Ändern von Farben, das Bewegen des Cursors und das Löschen von Bildschirminhalten bereitstellt.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
tput [Optionen] [Argumente]
```

## Häufige Optionen
- `setaf [FARBE]`: Setzt die Vordergrundfarbe auf die angegebene Farbe.
- `setab [FARBE]`: Setzt die Hintergrundfarbe auf die angegebene Farbe.
- `clear`: Löscht den Bildschirm.
- `cup [ZEILE] [SPALTE]`: Bewegt den Cursor zur angegebenen Zeile und Spalte.
- `bold`: Setzt den Text auf fett.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `tput`:

### Beispiel 1: Textfarbe ändern
Ändern Sie die Vordergrundfarbe auf Rot:
```bash
tput setaf 1
echo "Dieser Text ist rot."
```

### Beispiel 2: Hintergrundfarbe ändern
Ändern Sie die Hintergrundfarbe auf Blau:
```bash
tput setab 4
echo "Der Hintergrund ist blau."
```

### Beispiel 3: Bildschirm löschen
Löschen Sie den gesamten Bildschirm:
```bash
tput clear
```

### Beispiel 4: Cursorposition ändern
Bewegen Sie den Cursor zur Zeile 5 und Spalte 10:
```bash
tput cup 5 10
echo "Hier ist der Cursor."
```

### Beispiel 5: Fettgedruckten Text
Geben Sie fettgedruckten Text aus:
```bash
tput bold
echo "Dieser Text ist fett."
tput sgr0  # Setzt die Formatierung zurück
```

## Tipps
- Verwenden Sie `tput sgr0`, um alle Formatierungen zurückzusetzen und den Standardzustand wiederherzustellen.
- Experimentieren Sie mit verschiedenen Farbnummern, um die gewünschten Farben zu finden. Die Farbnummern variieren je nach Terminal.
- Kombinieren Sie mehrere `tput`-Befehle in einem Skript, um komplexe Terminalausgaben zu erstellen.