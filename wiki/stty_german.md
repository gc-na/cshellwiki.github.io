# [Linux] Bash stty Verwendung: Terminaleinstellungen ändern

## Übersicht
Der `stty`-Befehl wird verwendet, um die Terminaleinstellungen zu ändern und zu konfigurieren. Er ermöglicht es Benutzern, verschiedene Aspekte der Terminalkommunikation zu steuern, wie z.B. Eingabemodi, Ausgabemodi und Steuerzeichen.

## Verwendung
Die grundlegende Syntax des `stty`-Befehls lautet:

```bash
stty [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle aktuellen Einstellungen des Terminals an.
- `-g`: Gibt die aktuellen Einstellungen in einem Format aus, das später wieder verwendet werden kann.
- `erase`: Setzt das Zeichen, das zum Löschen des letzten Zeichens verwendet wird.
- `kill`: Setzt das Zeichen, das zum Löschen der gesamten Eingabezeile verwendet wird.
- `intr`: Setzt das Zeichen, das zum Unterbrechen eines laufenden Prozesses verwendet wird.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `stty`:

### Alle Terminaleinstellungen anzeigen
```bash
stty -a
```

### Eingabemodus ändern (z.B. das Löschen-Zeichen auf Backspace setzen)
```bash
stty erase ^H
```

### Zeichen für das Unterbrechen eines Prozesses setzen
```bash
stty intr ^C
```

### Aktuelle Einstellungen in einem wiederverwendbaren Format speichern
```bash
stty -g > settings.txt
```

### Einstellungen aus einer Datei wiederherstellen
```bash
stty $(cat settings.txt)
```

## Tipps
- Verwenden Sie `stty -a`, um einen Überblick über alle aktuellen Einstellungen zu erhalten, bevor Sie Änderungen vornehmen.
- Seien Sie vorsichtig beim Ändern von Steuerzeichen, da dies die Eingabe und Interaktion mit dem Terminal beeinflussen kann.
- Testen Sie Änderungen in einer sicheren Umgebung, um unerwartete Probleme zu vermeiden.