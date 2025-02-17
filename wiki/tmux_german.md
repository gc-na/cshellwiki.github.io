# [Linux] Bash tmux Verwendung: Terminal-Multiplexer

## Übersicht
Der `tmux` Befehl ist ein Terminal-Multiplexer, der es ermöglicht, mehrere Terminal-Sitzungen innerhalb eines einzigen Fensters zu verwalten. Dies ist besonders nützlich, um verschiedene Aufgaben gleichzeitig zu erledigen, ohne mehrere Terminalfenster öffnen zu müssen.

## Verwendung
Die grundlegende Syntax des `tmux` Befehls lautet:

```bash
tmux [Optionen] [Argumente]
```

## Häufige Optionen
- `new`: Erstellt eine neue tmux-Sitzung.
- `attach`: Verbindet sich mit einer bestehenden tmux-Sitzung.
- `list-sessions`: Listet alle aktiven tmux-Sitzungen auf.
- `kill-session`: Beendet eine tmux-Sitzung.
- `detach`: Trennt die Verbindung zur aktuellen tmux-Sitzung.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `tmux`:

1. **Neue tmux-Sitzung erstellen:**
   ```bash
   tmux new -s meine_sitzung
   ```

2. **Mit einer bestehenden Sitzung verbinden:**
   ```bash
   tmux attach -t meine_sitzung
   ```

3. **Alle aktiven Sitzungen auflisten:**
   ```bash
   tmux list-sessions
   ```

4. **Eine Sitzung beenden:**
   ```bash
   tmux kill-session -t meine_sitzung
   ```

5. **Sitzung trennen (ohne sie zu beenden):**
   Drücken Sie `Ctrl + b`, gefolgt von `d`.

## Tipps
- Verwenden Sie `tmux`-Tastenkombinationen, um effizient zwischen Fenstern und Paneelen zu navigieren.
- Benennen Sie Ihre Sitzungen sinnvoll, um die Verwaltung zu erleichtern.
- Nutzen Sie die Möglichkeit, mehrere Paneele innerhalb einer Sitzung zu erstellen, um verschiedene Aufgaben gleichzeitig zu erledigen.