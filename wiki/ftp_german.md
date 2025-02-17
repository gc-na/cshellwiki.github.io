# [Linux] Bash ftp Verwendung: Dateien über das FTP-Protokoll übertragen

## Übersicht
Der `ftp`-Befehl (File Transfer Protocol) wird verwendet, um Dateien zwischen einem lokalen Computer und einem Remote-Server über das FTP-Protokoll zu übertragen. Er ermöglicht das Hochladen, Herunterladen und Verwalten von Dateien auf einem FTP-Server.

## Verwendung
Die grundlegende Syntax des `ftp`-Befehls lautet:

```bash
ftp [Optionen] [Argumente]
```

## Häufige Optionen
- `-i`: Schaltet den interaktiven Modus aus, um die Übertragung mehrerer Dateien zu ermöglichen.
- `-n`: Verhindert die automatische Anmeldung beim FTP-Server.
- `-v`: Aktiviert den ausführlichen Modus, um mehr Informationen über den Verbindungsstatus anzuzeigen.
- `-p`: Verwendet passive Modusverbindungen, was bei Firewalls hilfreich sein kann.

## Häufige Beispiele

### Verbindung zu einem FTP-Server herstellen
Um eine Verbindung zu einem FTP-Server herzustellen, verwenden Sie den folgenden Befehl:

```bash
ftp ftp.example.com
```

### Anmelden mit Benutzername und Passwort
Um sich mit einem bestimmten Benutzernamen und Passwort anzumelden, verwenden Sie:

```bash
ftp -n ftp.example.com
user username password
```

### Dateien herunterladen
Um eine Datei von einem FTP-Server herunterzuladen, verwenden Sie den `get`-Befehl:

```bash
get datei.txt
```

### Dateien hochladen
Um eine Datei auf einen FTP-Server hochzuladen, verwenden Sie den `put`-Befehl:

```bash
put lokale_datei.txt
```

### Mehrere Dateien herunterladen
Um mehrere Dateien herunterzuladen, aktivieren Sie den interaktiven Modus und verwenden Sie den `mget`-Befehl:

```bash
ftp -i ftp.example.com
mget *.txt
```

## Tipps
- Verwenden Sie den `-v`-Schalter, um bei Verbindungsproblemen detaillierte Informationen zu erhalten.
- Nutzen Sie den passiven Modus (`-p`), wenn Sie hinter einer Firewall arbeiten.
- Achten Sie darauf, sensible Daten wie Passwörter sicher zu übertragen, indem Sie eine sichere Verbindung (z.B. SFTP) in Betracht ziehen.