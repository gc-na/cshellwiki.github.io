# [Linux] C Shell (csh) scp Verwendung: Dateien sicher kopieren

## Übersicht
Der `scp`-Befehl (Secure Copy Protocol) wird verwendet, um Dateien sicher zwischen einem lokalen und einem entfernten Host oder zwischen zwei entfernten Hosts zu kopieren. Er nutzt SSH (Secure Shell) zur Authentifizierung und zur Verschlüsselung der Datenübertragung.

## Verwendung
Die grundlegende Syntax des `scp`-Befehls lautet:

```csh
scp [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
- `-r`: Kopiert Verzeichnisse rekursiv.
- `-P`: Gibt den Port an, der für die Verbindung verwendet werden soll (beachten Sie, dass dies ein großes "P" ist).
- `-i`: Gibt die Datei mit dem privaten Schlüssel an, die für die Authentifizierung verwendet werden soll.
- `-v`: Aktiviert den ausführlichen Modus, um detaillierte Informationen über den Kopiervorgang anzuzeigen.

## Häufige Beispiele
1. **Eine Datei von lokal nach remote kopieren:**
   ```csh
   scp /pfad/zur/datei.txt benutzer@remotehost:/pfad/zum/ziel/
   ```

2. **Eine Datei von remote nach lokal kopieren:**
   ```csh
   scp benutzer@remotehost:/pfad/zur/datei.txt /pfad/zum/ziel/
   ```

3. **Ein ganzes Verzeichnis rekursiv kopieren:**
   ```csh
   scp -r /pfad/zum/verzeichnis benutzer@remotehost:/pfad/zum/ziel/
   ```

4. **Kopieren einer Datei über einen bestimmten Port:**
   ```csh
   scp -P 2222 /pfad/zur/datei.txt benutzer@remotehost:/pfad/zum/ziel/
   ```

5. **Kopieren einer Datei mit einem spezifischen privaten Schlüssel:**
   ```csh
   scp -i /pfad/zum/schluessel.pem /pfad/zur/datei.txt benutzer@remotehost:/pfad/zum/ziel/
   ```

## Tipps
- Stellen Sie sicher, dass der SSH-Dienst auf dem Zielhost läuft, um Verbindungsprobleme zu vermeiden.
- Verwenden Sie den `-v`-Schalter, um bei Problemen detaillierte Fehlermeldungen zu erhalten.
- Achten Sie darauf, die richtigen Berechtigungen für die Dateien und Verzeichnisse zu setzen, um Zugriffsprobleme zu vermeiden.