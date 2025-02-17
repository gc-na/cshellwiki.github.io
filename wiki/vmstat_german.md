# [Linux] Bash vmstat Verwendung: Überwachung von Systemressourcen

## Overview
Der `vmstat`-Befehl (Virtual Memory Statistics) ist ein nützliches Werkzeug zur Überwachung von Systemressourcen in Echtzeit. Er liefert Informationen über die Speichernutzung, den CPU-Status und andere Systemaktivitäten, was bei der Diagnose von Leistungsproblemen hilfreich ist.

## Usage
Die grundlegende Syntax des `vmstat`-Befehls lautet:

```bash
vmstat [Optionen] [Intervalle] [Anzahl]
```

## Common Options
- `-a`: Zeigt alle Speicherstatistiken an, einschließlich der aktiven und inaktiven Speicher.
- `-m`: Zeigt Informationen über den Speicherverbrauch von Slab-Cache-Objekten.
- `-s`: Gibt eine zusammenfassende Statistik über den Systemstatus aus.
- `-d`: Zeigt Statistiken über Blockgeräte an.
- `-w`: Wechselt in den "Wide"-Modus, um breitere Ausgaben zu ermöglichen.

## Common Examples
Hier sind einige praktische Beispiele für die Verwendung von `vmstat`:

1. **Grundlegende Systemstatistiken anzeigen:**
   ```bash
   vmstat
   ```

2. **Statistiken alle 5 Sekunden anzeigen:**
   ```bash
   vmstat 5
   ```

3. **Statistiken alle 5 Sekunden für 10 Intervalle anzeigen:**
   ```bash
   vmstat 5 10
   ```

4. **Speicherstatistiken im Detail anzeigen:**
   ```bash
   vmstat -a
   ```

5. **Statistiken über Blockgeräte anzeigen:**
   ```bash
   vmstat -d
   ```

## Tips
- Verwenden Sie `vmstat` in Kombination mit anderen Monitoring-Tools, um ein umfassenderes Bild der Systemleistung zu erhalten.
- Achten Sie darauf, die Intervalle und Anzahl der Abfragen so zu wählen, dass sie Ihren Überwachungsbedürfnissen entsprechen, um die Ausgabe übersichtlich zu halten.
- Nutzen Sie die Option `-s`, um eine schnelle Zusammenfassung der Systemstatistiken zu erhalten, die bei der Fehlersuche hilfreich sein kann.