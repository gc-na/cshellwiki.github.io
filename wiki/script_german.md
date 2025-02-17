# [Linux] Bash-Skript Verwendung: Erstellen von Aufzeichnungen von Terminal-Sitzungen

## Übersicht
Der `script` Befehl wird verwendet, um eine Aufzeichnung einer Terminal-Sitzung zu erstellen. Dies ist besonders nützlich, um alle Eingaben und Ausgaben während einer Sitzung zu speichern, was bei der Fehlersuche oder Dokumentation hilfreich sein kann.

## Verwendung
Die grundlegende Syntax des `script` Befehls lautet:

```bash
script [Optionen] [Dateiname]
```

## Häufige Optionen
- `-a`: Fügt die Ausgabe an eine bestehende Datei an, anstatt sie zu überschreiben.
- `-q`: Führt den Befehl im stillen Modus aus, ohne eine Begrüßungsnachricht anzuzeigen.
- `-t`: Erstellt eine Zeitstempel-Datei, die die Zeitstempel der Eingaben aufzeichnet.

## Häufige Beispiele

1. **Aufzeichnung einer Sitzung in einer Datei:**
   ```bash
   script aufzeichnung.txt
   ```
   Dies startet eine neue Sitzung und speichert alle Eingaben und Ausgaben in der Datei `aufzeichnung.txt`.

2. **Aufzeichnung im stillen Modus:**
   ```bash
   script -q aufzeichnung.txt
   ```
   Hierbei wird die Sitzung ebenfalls in `aufzeichnung.txt` aufgezeichnet, jedoch ohne Begrüßungsnachricht.

3. **Anfügen an eine bestehende Datei:**
   ```bash
   script -a aufzeichnung.txt
   ```
   Diese Option fügt die neue Sitzung an die bereits vorhandene Datei `aufzeichnung.txt` an.

4. **Aufzeichnung mit Zeitstempeln:**
   ```bash
   script -t aufzeichnung.txt
   ```
   Dies speichert die Sitzung in `aufzeichnung.txt` und erstellt zusätzlich eine Zeitstempel-Datei.

## Tipps
- Verwenden Sie `script` in Kombination mit anderen Befehlen, um spezifische Aufgaben zu dokumentieren.
- Überprüfen Sie die aufgezeichnete Datei nach der Sitzung, um sicherzustellen, dass alle benötigten Informationen erfasst wurden.
- Nutzen Sie die `-a` Option, wenn Sie mehrere Sitzungen in einer Datei zusammenfassen möchten, um eine vollständige Historie zu erstellen.