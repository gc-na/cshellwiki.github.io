# [Linux] C Shell (csh) tee Verwendung: Daten gleichzeitig ausgeben und speichern

## Übersicht
Der `tee` Befehl in der C Shell (csh) wird verwendet, um Eingabedaten gleichzeitig auf der Standardausgabe anzuzeigen und in eine oder mehrere Dateien zu schreiben. Dies ist besonders nützlich, wenn Sie die Ausgabe eines Befehls sowohl sehen als auch speichern möchten.

## Verwendung
Die grundlegende Syntax des `tee` Befehls lautet:

```csh
tee [optionen] [argumente]
```

## Häufige Optionen
- `-a`: Fügt die Ausgabe an die angegebene Datei an, anstatt sie zu überschreiben.
- `-i`: Ignoriert Interrupt-Signale.
- `-p`: Gibt die Ausgabe an die Standardausgabe und die angegebene Datei weiter.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `tee` Befehls:

1. **Einfaches Speichern der Ausgabe in eine Datei:**
   ```csh
   ls -l | tee dateiliste.txt
   ```
   Dies listet die Dateien im aktuellen Verzeichnis auf und speichert die Ausgabe in `dateiliste.txt`.

2. **Anfügen der Ausgabe an eine bestehende Datei:**
   ```csh
   echo "Neue Zeile" | tee -a dateiliste.txt
   ```
   Hier wird "Neue Zeile" an das Ende von `dateiliste.txt` angefügt.

3. **Gleichzeitige Ausgabe in mehrere Dateien:**
   ```csh
   echo "Testausgabe" | tee datei1.txt datei2.txt
   ```
   Diese Zeile gibt "Testausgabe" sowohl in `datei1.txt` als auch in `datei2.txt` aus.

4. **Verwendung mit einem anderen Befehl:**
   ```csh
   ps aux | tee laufende_prozesse.txt
   ```
   Dies speichert die Liste der laufenden Prozesse in `laufende_prozesse.txt` und zeigt sie gleichzeitig im Terminal an.

## Tipps
- Verwenden Sie die `-a` Option, wenn Sie Daten an eine bestehende Datei anhängen möchten, um Datenverlust zu vermeiden.
- Kombinieren Sie `tee` mit anderen Befehlen in einer Pipeline, um die Ausgabe effizient zu verarbeiten und zu speichern.
- Überprüfen Sie immer die Berechtigungen der Datei, in die Sie schreiben möchten, um sicherzustellen, dass Sie die erforderlichen Zugriffsrechte haben.