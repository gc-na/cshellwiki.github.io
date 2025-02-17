# [Linux] Bash htop Verwendung: Systemüberwachung und Prozessverwaltung

## Übersicht
Der Befehl `htop` ist ein interaktives Prozessanzeigetool für Unix-Systeme. Es bietet eine benutzerfreundliche Oberfläche zur Überwachung von Systemressourcen und Prozessen in Echtzeit. Im Gegensatz zu dem traditionellen `top`-Befehl bietet `htop` eine farbige Darstellung und ermöglicht eine einfachere Navigation und Interaktion.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
htop [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`, `--help`: Zeigt die Hilfe und eine Liste der Optionen an.
- `-s`, `--sort`: Ermöglicht das Sortieren der Prozesse nach einem bestimmten Kriterium (z.B. CPU, RAM).
- `-p`, `--pid`: Zeigt nur die Prozesse mit den angegebenen Prozess-IDs an.
- `-u`, `--user`: Filtert die Prozesse nach dem angegebenen Benutzernamen.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `htop`:

1. **Einfaches Starten von htop:**
   ```bash
   htop
   ```

2. **Sortieren nach CPU-Nutzung:**
   ```bash
   htop -s PERCENT_CPU
   ```

3. **Anzeigen von Prozessen eines bestimmten Benutzers:**
   ```bash
   htop -u benutzername
   ```

4. **Anzeigen von spezifischen Prozessen anhand ihrer PID:**
   ```bash
   htop -p 1234,5678
   ```

## Tipps
- Verwenden Sie die Pfeiltasten, um durch die Liste der Prozesse zu navigieren.
- Drücken Sie `F9`, um einen Prozess zu beenden, und wählen Sie das entsprechende Signal aus.
- Nutzen Sie die `F4`-Taste, um nach Prozessen zu filtern, und die `F5`-Taste, um die Baumansicht zu aktivieren, die die Hierarchie der Prozesse anzeigt.
- Passen Sie die Anzeige an, indem Sie `F2` drücken, um die Einstellungen zu öffnen und verschiedene Optionen zu konfigurieren.