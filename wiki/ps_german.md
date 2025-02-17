# [Linux] Bash ps Verwendung: Prozesse anzeigen

## Übersicht
Der `ps`-Befehl wird in Unix-ähnlichen Betriebssystemen verwendet, um Informationen über die aktuell laufenden Prozesse anzuzeigen. Er bietet eine Momentaufnahme der Prozesse, die auf dem System aktiv sind, und zeigt wichtige Details wie Prozess-ID, CPU- und Speicherauslastung.

## Verwendung
Die grundlegende Syntax des `ps`-Befehls lautet:

```bash
ps [Optionen] [Argumente]
```

## Häufige Optionen
- `-e` oder `-A`: Zeigt alle Prozesse an.
- `-f`: Zeigt die Prozesse in einem vollständigen Format an, einschließlich der Elternprozess-ID.
- `-u [Benutzer]`: Zeigt die Prozesse für einen bestimmten Benutzer an.
- `-aux`: Zeigt alle Prozesse mit detaillierten Informationen an (eine Kombination von Optionen).
- `--sort`: Sortiert die Ausgabe nach einem bestimmten Kriterium, z.B. `--sort=-%mem` für die Speicherauslastung.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `ps`-Befehls:

1. **Alle Prozesse anzeigen:**
   ```bash
   ps -e
   ```

2. **Detaillierte Informationen über alle Prozesse:**
   ```bash
   ps aux
   ```

3. **Prozesse eines bestimmten Benutzers anzeigen:**
   ```bash
   ps -u username
   ```

4. **Prozesse nach Speicherauslastung sortieren:**
   ```bash
   ps aux --sort=-%mem
   ```

5. **Vollständige Informationen über einen bestimmten Prozess anzeigen:**
   ```bash
   ps -f -p 1234
   ```

## Tipps
- Verwenden Sie `ps aux | grep [Suchbegriff]`, um nach einem bestimmten Prozess zu suchen.
- Kombinieren Sie `ps` mit anderen Befehlen wie `less`, um die Ausgabe besser lesen zu können: 
  ```bash
  ps aux | less
  ```
- Nutzen Sie `htop` oder `top` für eine dynamische und interaktive Ansicht der Prozesse, wenn Sie eine kontinuierliche Überwachung benötigen.