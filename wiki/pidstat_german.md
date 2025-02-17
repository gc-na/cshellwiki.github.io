# [Linux] Bash pidstat Verwendung: Überwachung von Prozessstatistiken

## Übersicht
Der Befehl `pidstat` ist ein nützliches Tool zur Überwachung von Prozessstatistiken in Echtzeit. Es zeigt Informationen über CPU-Nutzung, Speicherverbrauch und andere Leistungsmetriken für laufende Prozesse an. Dies ist besonders hilfreich für Systemadministratoren und Entwickler, die die Leistung ihrer Anwendungen analysieren möchten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
pidstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Zeigt die Hilfe an und listet alle verfügbaren Optionen auf.
- `-r`: Zeigt die Speichernutzung der Prozesse an.
- `-u`: Zeigt die CPU-Nutzung der Prozesse an.
- `-p <PID>`: Überwacht einen spezifischen Prozess anhand seiner Prozess-ID (PID).
- `-t`: Zeigt die Statistiken für Threads an.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `pidstat`:

1. **CPU-Nutzung aller Prozesse anzeigen**:
   ```bash
   pidstat -u
   ```

2. **Speichernutzung für alle Prozesse anzeigen**:
   ```bash
   pidstat -r
   ```

3. **Überwachung eines spezifischen Prozesses (z.B. PID 1234)**:
   ```bash
   pidstat -p 1234
   ```

4. **Statistiken für Threads eines Prozesses anzeigen**:
   ```bash
   pidstat -t -p 1234
   ```

5. **CPU- und Speichernutzung alle 2 Sekunden anzeigen**:
   ```bash
   pidstat -u -r 2
   ```

## Tipps
- Verwenden Sie die Option `-h`, um eine vollständige Liste der verfügbaren Optionen zu erhalten und sich mit den Funktionen vertraut zu machen.
- Kombinieren Sie `pidstat` mit anderen Befehlen wie `grep`, um spezifische Prozesse zu filtern.
- Nutzen Sie die Möglichkeit, Statistiken über einen längeren Zeitraum zu sammeln, indem Sie die Abfrageintervalle anpassen, um Trends in der Nutzung zu erkennen.