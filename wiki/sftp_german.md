# [Linux] C Shell (csh) sftp Verwendung: Dateien sicher übertragen

## Übersicht
Der `sftp`-Befehl (SSH File Transfer Protocol) wird verwendet, um Dateien sicher zwischen einem lokalen und einem entfernten Computer zu übertragen. Er bietet eine sichere Möglichkeit, Dateien über das Netzwerk zu übertragen, indem er die SSH-Verschlüsselung nutzt.

## Verwendung
Die grundlegende Syntax des `sftp`-Befehls lautet:

```bash
sftp [Optionen] [Benutzername@Host]
```

## Häufige Optionen
- `-P <Port>`: Gibt den Port an, der für die Verbindung verwendet werden soll.
- `-o <Option>`: Ermöglicht das Setzen von SSH-Optionen.
- `-v`: Aktiviert den ausführlichen Modus, um mehr Informationen über die Verbindung zu erhalten.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `sftp`:

1. **Verbindung zu einem entfernten Server herstellen:**
   ```bash
   sftp benutzername@hostname
   ```

2. **Datei vom lokalen Computer auf den entfernten Server hochladen:**
   ```bash
   sftp benutzername@hostname
   put lokale_datei.txt
   ```

3. **Datei vom entfernten Server auf den lokalen Computer herunterladen:**
   ```bash
   sftp benutzername@hostname
   get entfernte_datei.txt
   ```

4. **Verzeichnisinhalt auf dem entfernten Server auflisten:**
   ```bash
   sftp benutzername@hostname
   ls
   ```

5. **Mehrere Dateien hochladen:**
   ```bash
   sftp benutzername@hostname
   mput datei1.txt datei2.txt
   ```

## Tipps
- Verwenden Sie den `-v`-Schalter, um Verbindungsprobleme leichter zu diagnostizieren.
- Stellen Sie sicher, dass der SSH-Dienst auf dem entfernten Server läuft, bevor Sie eine Verbindung herstellen.
- Nutzen Sie `exit` oder `bye`, um die sftp-Sitzung sicher zu beenden.