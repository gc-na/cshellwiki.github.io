# [Linux] C Shell (csh) tmux Verwendung: Terminal-Multiplexer

## Übersicht
Der Befehl `tmux` ist ein Terminal-Multiplexer, der es ermöglicht, mehrere Terminal-Sitzungen innerhalb eines einzigen Fensters zu verwalten. Mit tmux können Benutzer zwischen verschiedenen Sitzungen wechseln, Fenster teilen und ihre Arbeit in einer persistenten Umgebung fortsetzen.

## Verwendung
Die grundlegende Syntax des `tmux`-Befehls lautet:

```bash
tmux [Optionen] [Argumente]
```

## Häufige Optionen
- `new`: Erstellt eine neue tmux-Sitzung.
- `attach`: Verbindet sich mit einer bestehenden tmux-Sitzung.
- `list-sessions`: Listet alle aktiven tmux-Sitzungen auf.
- `kill-session`: Beendet eine tmux-Sitzung.
- `detach`: Trennt die aktuelle tmux-Sitzung.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von tmux:

### Neue Sitzung erstellen
```bash
tmux new -s meine_sitzung
```

### Bestehende Sitzung anhängen
```bash
tmux attach -t meine_sitzung
```

### Alle Sitzungen auflisten
```bash
tmux list-sessions
```

### Sitzung beenden
```bash
tmux kill-session -t meine_sitzung
```

### Sitzung trennen
```bash
Ctrl-b d
```

## Tipps
- Verwenden Sie `tmux`-Tastenkombinationen (z.B. `Ctrl-b` gefolgt von `c`), um schnell neue Fenster zu erstellen.
- Nutzen Sie die Möglichkeit, Fenster horizontal oder vertikal zu teilen, um mehrere Aufgaben gleichzeitig zu erledigen.
- Speichern Sie Ihre tmux-Konfiguration in einer `.tmux.conf`-Datei, um benutzerdefinierte Einstellungen zu laden.