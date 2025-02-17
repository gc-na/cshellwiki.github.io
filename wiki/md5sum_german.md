# [Linux] Bash md5sum Verwendung: Berechnung von MD5-Prüfziffern

## Übersicht
Der Befehl `md5sum` wird verwendet, um die MD5-Prüfziffer (Checksumme) einer Datei zu berechnen. Diese Prüfziffer wird häufig verwendet, um die Integrität von Dateien zu überprüfen und sicherzustellen, dass sie nicht verändert wurden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
md5sum [Optionen] [Argumente]
```

## Häufige Optionen
- `-b`: Behandelt die Eingabedatei als Binärdatei.
- `-c`: Überprüft die Prüfziffern einer Datei, die zuvor mit `md5sum` erstellt wurde.
- `-t`: Berechnet die Prüfziffer für die Eingabe von Standard-Input (stdin).
- `--help`: Zeigt eine Hilfeseite mit Informationen zur Verwendung des Befehls an.

## Häufige Beispiele

### Berechnung der MD5-Prüfziffer einer Datei
Um die MD5-Prüfziffer einer Datei zu berechnen, verwenden Sie den folgenden Befehl:

```bash
md5sum dateiname.txt
```

### Berechnung der MD5-Prüfziffer für mehrere Dateien
Um die MD5-Prüfzifferen mehrerer Dateien gleichzeitig zu berechnen, geben Sie die Dateinamen einfach hintereinander an:

```bash
md5sum datei1.txt datei2.txt datei3.txt
```

### Überprüfung einer MD5-Prüfziffer
Wenn Sie eine Datei haben, die eine Liste von MD5-Prüfziffern enthält, können Sie diese mit dem folgenden Befehl überprüfen:

```bash
md5sum -c checksummen.txt
```

### MD5-Prüfziffer von Standard-Input
Um die MD5-Prüfziffer von Daten zu berechnen, die über die Standard-Eingabe eingegeben werden, verwenden Sie:

```bash
echo "Beispieltext" | md5sum
```

## Tipps
- Speichern Sie die MD5-Prüfziffern in einer Datei, um die Integrität wichtiger Dateien regelmäßig zu überprüfen.
- Verwenden Sie `-b`, wenn Sie mit Binärdateien arbeiten, um genaue Ergebnisse zu gewährleisten.
- Seien Sie sich bewusst, dass MD5 nicht als sicher gilt für kryptografische Anwendungen; für sicherheitskritische Anwendungen sollten Sie stärkere Algorithmen wie SHA-256 in Betracht ziehen.