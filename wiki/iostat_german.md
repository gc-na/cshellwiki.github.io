# [Linux] C Shell (csh) iostat Verwendung: Überwachung von CPU- und I/O-Leistung

## Übersicht
Der Befehl `iostat` wird verwendet, um Informationen über die CPU- und I/O-Leistung des Systems anzuzeigen. Er hilft dabei, Engpässe in der Leistung zu identifizieren, indem er Statistiken über die Nutzung von Festplatten und anderen Speichermedien bereitstellt.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
iostat [Optionen] [Argumente]
```

## Häufige Optionen
- `-c`: Zeigt nur die CPU-Statistiken an.
- `-d`: Zeigt nur die I/O-Geräte-Statistiken an.
- `-x`: Zeigt erweiterte Statistiken für die I/O-Geräte an.
- `-t`: Fügt einen Zeitstempel zu den Ausgaben hinzu.
- `-h`: Gibt die Ausgabe in einem menschenlesbaren Format (z. B. MB/s) aus.

## Häufige Beispiele

1. **CPU-Statistiken anzeigen:**
   ```bash
   iostat -c
   ```

2. **I/O-Geräte-Statistiken anzeigen:**
   ```bash
   iostat -d
   ```

3. **Erweiterte Statistiken für I/O-Geräte anzeigen:**
   ```bash
   iostat -x
   ```

4. **Statistiken alle 5 Sekunden aktualisieren:**
   ```bash
   iostat 5
   ```

5. **Statistiken mit Zeitstempel anzeigen:**
   ```bash
   iostat -t
   ```

## Tipps
- Verwenden Sie die Option `-h`, um die Ausgabe leichter lesbar zu machen, insbesondere bei großen Datenmengen.
- Kombinieren Sie Optionen, um spezifische Informationen zu erhalten, z. B. `iostat -c -d` für CPU- und I/O-Statistiken gleichzeitig.
- Überwachen Sie die Statistiken über einen längeren Zeitraum, um Trends in der Systemleistung zu erkennen.