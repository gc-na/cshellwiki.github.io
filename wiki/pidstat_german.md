# [Linux] C Shell (csh) pidstat: Prozessstatistiken anzeigen

## Übersicht
Der Befehl `pidstat` wird verwendet, um die CPU- und Speicherverbrauchsstatistiken von Prozessen in Echtzeit anzuzeigen. Er ist besonders nützlich, um die Leistung von Prozessen zu überwachen und Engpässe zu identifizieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
pidstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Zeigt die Statistiken in einem menschenlesbaren Format an.
- `-r`: Zeigt den Speicherverbrauch der Prozesse an.
- `-p <PID>`: Überwacht einen spezifischen Prozess anhand seiner Prozess-ID.
- `-u`: Zeigt die CPU-Nutzung der Prozesse an.
- `-t`: Zeigt die Statistiken für alle Threads eines Prozesses an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `pidstat`:

1. **CPU-Nutzung aller Prozesse anzeigen:**
   ```bash
   pidstat -u
   ```

2. **Speicherverbrauch eines spezifischen Prozesses überwachen:**
   ```bash
   pidstat -r -p 1234
   ```

3. **Statistiken für alle Threads eines Prozesses anzeigen:**
   ```bash
   pidstat -t -p 5678
   ```

4. **Statistiken alle 5 Sekunden aktualisieren:**
   ```bash
   pidstat 5
   ```

## Tipps
- Verwenden Sie die Option `-h`, um die Ausgabe besser lesbar zu machen, insbesondere bei großen Datenmengen.
- Kombinieren Sie Optionen, um umfassendere Informationen zu erhalten, z.B. `pidstat -u -r`.
- Überwachen Sie regelmäßig die Prozesse, um potenzielle Leistungsprobleme frühzeitig zu erkennen.