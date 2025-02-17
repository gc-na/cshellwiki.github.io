# [Linux] Bash iotop Verwendung: Überwachung der I/O-Aktivität von Prozessen

## Übersicht
Das `iotop`-Kommando ist ein nützliches Tool zur Überwachung der Ein- und Ausgabeaktivität (I/O) von Prozessen in Echtzeit. Es zeigt an, welche Prozesse die meiste I/O-Leistung beanspruchen, was bei der Fehlersuche und Optimierung von Systemressourcen hilfreich ist.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
iotop [Optionen] [Argumente]
```

## Häufige Optionen
- `-o`, `--only`: Zeigt nur Prozesse an, die aktuell I/O-Aktivität haben.
- `-b`, `--batch`: Führt `iotop` im Batch-Modus aus, nützlich für die Ausgabe in eine Datei.
- `-n NUM`, `--iter=NUM`: Gibt an, wie oft die Ausgabe aktualisiert werden soll (z. B. `-n 5` für 5 Aktualisierungen).
- `-d SEC`, `--delay=SEC`: Legt die Verzögerung zwischen den Aktualisierungen in Sekunden fest.

## Häufige Beispiele
1. **Standardausgabe von iotop**:
   ```bash
   iotop
   ```

2. **Nur Prozesse mit I/O-Aktivität anzeigen**:
   ```bash
   iotop -o
   ```

3. **Batch-Modus mit 10 Sekunden Verzögerung und 5 Iterationen**:
   ```bash
   iotop -b -n 5 -d 10
   ```

4. **Ausgabe in eine Datei umleiten**:
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

## Tipps
- Verwenden Sie den Batch-Modus, wenn Sie die Ausgabe in eine Datei speichern möchten, um die I/O-Aktivität über einen bestimmten Zeitraum zu protokollieren.
- Kombinieren Sie die Optionen `-o` und `-d`, um gezielt Prozesse mit I/O-Aktivität in festgelegten Intervallen zu überwachen.
- Achten Sie darauf, `iotop` mit Root-Rechten auszuführen, um vollständige Informationen zu erhalten.