# [Linux] C Shell (csh) wget Verwendung: Dateien aus dem Internet herunterladen

## Übersicht
Der `wget` Befehl ist ein leistungsstarkes Tool, das es ermöglicht, Dateien aus dem Internet herunterzuladen. Es unterstützt verschiedene Protokolle wie HTTP, HTTPS und FTP und kann sowohl einfache Downloads als auch komplexere Aufgaben wie das Herunterladen von ganzen Webseiten durchführen.

## Verwendung
Die grundlegende Syntax des `wget` Befehls lautet:

```bash
wget [Optionen] [Argumente]
```

## Häufige Optionen
- `-O <Dateiname>`: Speichert die heruntergeladene Datei unter dem angegebenen Namen.
- `-c`: Setzt einen abgebrochenen Download fort.
- `-r`: Aktiviert den rekursiven Download, um ganze Verzeichnisse herunterzuladen.
- `-p`: Lädt alle notwendigen Dateien für die Anzeige einer Webseite herunter (z.B. Bilder, CSS).
- `--limit-rate=<Rate>`: Begrenzung der Downloadgeschwindigkeit.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `wget`:

1. **Einzelne Datei herunterladen:**
   ```bash
   wget https://example.com/datei.zip
   ```

2. **Datei unter einem bestimmten Namen speichern:**
   ```bash
   wget -O mein_datei.zip https://example.com/datei.zip
   ```

3. **Download fortsetzen:**
   ```bash
   wget -c https://example.com/große_datei.zip
   ```

4. **Rekursiven Download eines gesamten Verzeichnisses:**
   ```bash
   wget -r https://example.com/verzeichnis/
   ```

5. **Webseite mit allen notwendigen Dateien herunterladen:**
   ```bash
   wget -p https://example.com
   ```

## Tipps
- Verwenden Sie die Option `-c`, um Downloads fortzusetzen, wenn die Verbindung unterbrochen wird.
- Nutzen Sie `--limit-rate`, um die Bandbreite zu steuern, insbesondere wenn Sie mehrere Downloads gleichzeitig durchführen.
- Überprüfen Sie die heruntergeladenen Dateien regelmäßig, um sicherzustellen, dass sie vollständig und nicht beschädigt sind.