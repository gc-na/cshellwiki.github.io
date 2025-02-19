# [Linux] C Shell (csh) screen Verwendung: Ein Terminal-Multiplexer

## Übersicht
Der `screen` Befehl ist ein Terminal-Multiplexer, der es Benutzern ermöglicht, mehrere Terminal-Sitzungen innerhalb eines einzigen Fensters zu verwalten. Mit `screen` können Sie Sitzungen im Hintergrund laufen lassen und später wieder darauf zugreifen, was besonders nützlich ist, wenn Sie lange laufende Prozesse haben.

## Verwendung
Die grundlegende Syntax des `screen` Befehls lautet:

```
screen [Optionen] [Argumente]
```

## Häufige Optionen
- `-S <name>`: Gibt einen Namen für die neue Sitzung an.
- `-d -r <name>`: Trennt eine Sitzung und verbindet sich erneut mit ihr.
- `-list`: Listet alle aktiven `screen` Sitzungen auf.
- `-r <name>`: Stellt eine bestehende Sitzung wieder her.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `screen`:

1. **Neue `screen` Sitzung erstellen:**
   ```bash
   screen -S meine_sitzung
   ```

2. **Sitzung trennen (detach):**
   Drücken Sie `Ctrl-a` gefolgt von `d`, um die Sitzung zu trennen.

3. **Wiederherstellen einer getrennten Sitzung:**
   ```bash
   screen -r meine_sitzung
   ```

4. **Auflisten aller aktiven `screen` Sitzungen:**
   ```bash
   screen -list
   ```

5. **Wiederherstellen einer Sitzung, die nicht benannt wurde:**
   ```bash
   screen -r 12345
   ```

## Tipps
- Verwenden Sie `screen` in Kombination mit `nohup`, um sicherzustellen, dass Ihre Prozesse auch nach dem Abmelden weiterlaufen.
- Benennen Sie Ihre Sitzungen mit `-S`, um die Verwaltung mehrerer Sitzungen zu erleichtern.
- Nutzen Sie die Funktionalität von `screen` zur Aufzeichnung von Sitzungen, um später auf die Ausgaben zugreifen zu können.