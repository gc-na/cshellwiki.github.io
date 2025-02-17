# [Linux] Bash dstat Verwendung: Systemressourcen überwachen

## Übersicht
Der Befehl `dstat` ist ein vielseitiges Tool zur Überwachung von Systemressourcen in Echtzeit. Es kombiniert die Funktionen von verschiedenen anderen Überwachungswerkzeugen und zeigt Informationen über CPU, Speicher, Netzwerk und andere Systemressourcen an.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
dstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-c`: Zeigt die CPU-Nutzung an.
- `-d`: Zeigt die Disk-I/O-Statistiken an.
- `-n`: Zeigt die Netzwerkstatistiken an.
- `-m`: Zeigt die Speichernutzung an.
- `--help`: Zeigt die Hilfe und eine Liste der verfügbaren Optionen an.

## Häufige Beispiele

1. **CPU- und Speicherstatistiken anzeigen:**
   ```bash
   dstat -c -m
   ```

2. **Disk- und Netzwerkstatistiken anzeigen:**
   ```bash
   dstat -d -n
   ```

3. **Alle Statistiken in Echtzeit anzeigen:**
   ```bash
   dstat
   ```

4. **Statistiken für einen bestimmten Zeitraum anzeigen (z.B. 10 Sekunden):**
   ```bash
   dstat 10
   ```

5. **Statistiken in eine Datei speichern:**
   ```bash
   dstat > dstat_output.txt
   ```

## Tipps
- Verwenden Sie `dstat` in Kombination mit anderen Befehlen wie `grep`, um spezifische Informationen zu filtern.
- Nutzen Sie die Option `--output`, um die Ausgabe in eine CSV-Datei zu speichern, die später analysiert werden kann.
- Experimentieren Sie mit verschiedenen Optionen, um die für Ihre Bedürfnisse relevantesten Statistiken anzuzeigen.