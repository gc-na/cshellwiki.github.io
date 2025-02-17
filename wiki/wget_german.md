# [Linux] Bash wget Verwendung: Dateien herunterladen

## Übersicht
Der `wget`-Befehl ist ein leistungsstarkes Tool zum Herunterladen von Dateien über das Internet. Er unterstützt verschiedene Protokolle wie HTTP, HTTPS und FTP und ist besonders nützlich, um Dateien automatisiert und im Hintergrund herunterzuladen.

## Verwendung
Die grundlegende Syntax des `wget`-Befehls lautet:

```bash
wget [Optionen] [Argumente]
```

## Häufige Optionen
Hier sind einige gängige Optionen für `wget`:

- `-O <Dateiname>`: Speichert die heruntergeladene Datei unter einem bestimmten Namen.
- `-c`: Setzt einen unterbrochenen Download fort.
- `-q`: Führt den Download im stillen Modus aus (keine Ausgabe).
- `--limit-rate=<Rate>`: Begrenzung der Downloadgeschwindigkeit.
- `-r`: Aktiviert den rekursiven Download von Webseiten.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `wget`:

1. **Einzelne Datei herunterladen:**
   ```bash
   wget https://example.com/datei.zip
   ```

2. **Datei mit einem bestimmten Namen speichern:**
   ```bash
   wget -O meinDatei.zip https://example.com/datei.zip
   ```

3. **Download fortsetzen:**
   ```bash
   wget -c https://example.com/datei.zip
   ```

4. **Rekursiven Download einer Webseite:**
   ```bash
   wget -r https://example.com
   ```

5. **Download mit Geschwindigkeitsbegrenzung:**
   ```bash
   wget --limit-rate=100k https://example.com/datei.zip
   ```

## Tipps
- Verwenden Sie die Option `-q`, wenn Sie den Download im Hintergrund durchführen möchten, um die Konsole nicht zu überladen.
- Nutzen Sie die rekursive Download-Option mit Bedacht, da sie viele Dateien herunterladen kann und viel Bandbreite benötigt.
- Überprüfen Sie die heruntergeladenen Dateien regelmäßig, um sicherzustellen, dass sie vollständig und nicht beschädigt sind.