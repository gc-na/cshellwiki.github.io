# [Linux] Bash tee Verwendung: Daten in Dateien umleiten und gleichzeitig anzeigen

## Übersicht
Der `tee` Befehl in Bash wird verwendet, um die Ausgabe eines Befehls sowohl auf dem Bildschirm anzuzeigen als auch in eine oder mehrere Dateien zu schreiben. Dies ist besonders nützlich, wenn Sie die Ausgabe eines Befehls überwachen und gleichzeitig speichern möchten.

## Verwendung
Die grundlegende Syntax des `tee` Befehls lautet:

```bash
tee [Optionen] [Datei(en)]
```

## Häufige Optionen
- `-a` oder `--append`: Fügt die Ausgabe an das Ende der angegebenen Datei an, anstatt sie zu überschreiben.
- `-i` oder `--ignore-interrupts`: Ignoriert Interrupt-Signale.
- `--help`: Zeigt eine Hilfe-Seite mit Informationen zur Verwendung von `tee`.
- `--version`: Gibt die Version des `tee` Befehls aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `tee`:

### Beispiel 1: Ausgabe in eine Datei schreiben
```bash
echo "Hallo Welt" | tee datei.txt
```
Dieser Befehl zeigt "Hallo Welt" auf dem Bildschirm an und speichert es gleichzeitig in `datei.txt`.

### Beispiel 2: Ausgabe an mehrere Dateien senden
```bash
echo "Daten speichern" | tee datei1.txt datei2.txt
```
Hier wird die Ausgabe sowohl in `datei1.txt` als auch in `datei2.txt` geschrieben.

### Beispiel 3: Ausgabe an eine Datei anhängen
```bash
echo "Zusätzliche Daten" | tee -a datei.txt
```
Dieser Befehl fügt "Zusätzliche Daten" am Ende von `datei.txt` hinzu, anstatt die Datei zu überschreiben.

### Beispiel 4: Verwendung mit anderen Befehlen
```bash
ls -l | tee dateiliste.txt
```
Hier wird die detaillierte Liste der Dateien im aktuellen Verzeichnis angezeigt und gleichzeitig in `dateiliste.txt` gespeichert.

## Tipps
- Verwenden Sie die `-a` Option, wenn Sie sicherstellen möchten, dass bestehende Daten in einer Datei nicht überschrieben werden.
- Kombinieren Sie `tee` mit anderen Befehlen in einer Pipeline, um die Ausgabe zu überwachen und gleichzeitig zu speichern.
- Nutzen Sie `tee` in Skripten, um Protokolle zu erstellen und die Ausgaben für die spätere Analyse zu speichern.