# [Linux] Bash sftp Verwendung: Sicherer Dateiübertragungsprotokoll

## Übersicht
Der `sftp`-Befehl (Secure File Transfer Protocol) wird verwendet, um Dateien sicher zwischen Computern über ein Netzwerk zu übertragen. Er bietet eine sichere Alternative zu FTP, indem er die Datenübertragung verschlüsselt.

## Verwendung
Die grundlegende Syntax des `sftp`-Befehls lautet:

```bash
sftp [Optionen] [Benutzername@Host]
```

## Häufige Optionen
- `-P`: Gibt den Port an, der für die Verbindung verwendet werden soll.
- `-o`: Ermöglicht das Setzen von spezifischen SSH-Optionen.
- `-v`: Aktiviert den ausführlichen Modus, um mehr Informationen über den Verbindungsprozess zu erhalten.

## Häufige Beispiele
- **Verbindung zu einem Remote-Server herstellen:**

```bash
sftp benutzername@hostname
```

- **Datei von einem Remote-Server herunterladen:**

```bash
sftp benutzername@hostname
get remote_datei.txt
```

- **Datei auf einen Remote-Server hochladen:**

```bash
sftp benutzername@hostname
put lokale_datei.txt
```

- **Verzeichnis auf dem Remote-Server auflisten:**

```bash
sftp benutzername@hostname
ls
```

## Tipps
- Verwenden Sie den `-v`-Schalter, um Verbindungsprobleme besser zu diagnostizieren.
- Speichern Sie häufig verwendete Verbindungsinformationen in einer SSH-Konfigurationsdatei, um die Eingabe zu erleichtern.
- Achten Sie darauf, sensible Daten sicher zu übertragen und verwenden Sie starke Passwörter für Ihre Benutzerkonten.