# [Linux] Bash mpstat Verwendung: Überwachung der CPU-Auslastung

## Übersicht
Der Befehl `mpstat` wird verwendet, um die CPU-Auslastung auf einem Linux-System zu überwachen. Er zeigt Statistiken über die CPU-Nutzung an, einschließlich der Auslastung pro CPU-Kern, was nützlich ist, um Engpässe oder Leistungsprobleme zu identifizieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
mpstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-P ALL`: Zeigt Statistiken für alle CPUs an.
- `-u`: Zeigt die CPU-Auslastung in Prozent an.
- `-h`: Gibt die Ausgabe in einem menschenlesbaren Format aus.
- `-o DATEINAME`: Speichert die Ausgabe in einer Datei.
- `interval`: Gibt das Intervall in Sekunden an, in dem die Statistiken aktualisiert werden sollen.
- `count`: Gibt die Anzahl der gewünschten Ausgaben an.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `mpstat`:

1. **CPU-Auslastung für alle CPUs anzeigen**:
   ```bash
   mpstat -P ALL
   ```

2. **CPU-Auslastung alle 2 Sekunden anzeigen**:
   ```bash
   mpstat 2
   ```

3. **CPU-Auslastung für alle CPUs und in menschenlesbarem Format anzeigen**:
   ```bash
   mpstat -P ALL -h
   ```

4. **Ausgabe in eine Datei speichern**:
   ```bash
   mpstat -P ALL -o output.txt
   ```

5. **CPU-Auslastung für eine bestimmte Anzahl von Abfragen anzeigen**:
   ```bash
   mpstat 1 5
   ```

## Tipps
- Verwenden Sie `mpstat -P ALL`, um eine detaillierte Übersicht über die Nutzung jeder CPU zu erhalten, besonders bei Mehrkernprozessoren.
- Kombinieren Sie `mpstat` mit anderen Befehlen wie `grep`, um spezifische Informationen herauszufiltern.
- Überwachen Sie die CPU-Auslastung während intensiver Anwendungen, um Engpässe zu identifizieren und die Leistung zu optimieren.