# [Linux] Bash scp Verwendung: Dateien sicher kopieren

## Übersicht
Der `scp` (Secure Copy Protocol) Befehl wird verwendet, um Dateien sicher zwischen einem lokalen und einem entfernten System oder zwischen zwei entfernten Systemen zu kopieren. Er nutzt SSH zur Authentifizierung und Verschlüsselung der Datenübertragung.

## Verwendung
Die grundlegende Syntax des `scp` Befehls lautet:

```bash
scp [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
- `-r`: Kopiert Verzeichnisse rekursiv.
- `-P`: Gibt den Port an, der für die Verbindung verwendet werden soll (beachten Sie, dass es ein großes "P" ist).
- `-i`: Gibt den Pfad zu einer privaten Schlüsseldatei an, die für die Authentifizierung verwendet wird.
- `-v`: Aktiviert den ausführlichen Modus, um mehr Informationen über den Kopiervorgang zu erhalten.

## Häufige Beispiele
1. **Eine Datei von lokal nach remote kopieren:**
   ```bash
   scp /pfad/zur/datei.txt benutzer@remote-server:/pfad/zum/ziel/
   ```

2. **Eine Datei von remote nach lokal kopieren:**
   ```bash
   scp benutzer@remote-server:/pfad/zur/datei.txt /pfad/zum/ziel/
   ```

3. **Ein ganzes Verzeichnis rekursiv kopieren:**
   ```bash
   scp -r /pfad/zum/verzeichnis benutzer@remote-server:/pfad/zum/ziel/
   ```

4. **Eine Datei über einen bestimmten Port kopieren:**
   ```bash
   scp -P 2222 /pfad/zur/datei.txt benutzer@remote-server:/pfad/zum/ziel/
   ```

5. **Eine Datei mit einer spezifischen privaten Schlüsseldatei kopieren:**
   ```bash
   scp -i /pfad/zur/schluesseldatei.pem /pfad/zur/datei.txt benutzer@remote-server:/pfad/zum/ziel/
   ```

## Tipps
- Verwenden Sie den `-v` Schalter, um bei Problemen mehr Informationen über den Kopiervorgang zu erhalten.
- Achten Sie darauf, die richtigen Berechtigungen für Ihre Schlüsseldateien zu setzen, um Verbindungsprobleme zu vermeiden.
- Nutzen Sie `scp` für schnelle und sichere Dateiübertragungen, insbesondere wenn Sie mit sensiblen Daten arbeiten.