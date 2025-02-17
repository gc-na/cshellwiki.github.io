# [Linux] Bash cksum Verwendung: Berechnung von Prüfziffern

## Übersicht
Der Befehl `cksum` berechnet die Prüfziffer (Checksumme) einer Datei und gibt die Anzahl der Bytes sowie die Prüfziffer selbst aus. Dies ist nützlich, um die Integrität von Dateien zu überprüfen und sicherzustellen, dass sie nicht verändert wurden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
cksum [Optionen] [Argumente]
```

## Häufige Optionen
- `-a, --algorithm=ALGO`: Wählt den Algorithmus für die Prüfziffer aus (z. B. `md5`, `sha256`).
- `--help`: Zeigt eine Hilfe-Seite mit Informationen zur Verwendung des Befehls an.
- `--version`: Gibt die Versionsnummer des `cksum`-Befehls aus.

## Häufige Beispiele
1. **Prüfziffer einer Datei berechnen:**
   ```bash
   cksum datei.txt
   ```
   Dieser Befehl gibt die Prüfziffer, die Anzahl der Bytes und den Dateinamen aus.

2. **Prüfziffer mehrerer Dateien berechnen:**
   ```bash
   cksum datei1.txt datei2.txt
   ```
   Hier werden die Prüfziffern für beide Dateien angezeigt.

3. **Prüfziffer mit einem bestimmten Algorithmus:**
   ```bash
   cksum --algorithm=md5 datei.txt
   ```
   Dieser Befehl verwendet den MD5-Algorithmus zur Berechnung der Prüfziffer.

## Tipps
- Verwenden Sie `cksum` in Kombination mit anderen Befehlen wie `find`, um die Prüfziffern für eine große Anzahl von Dateien zu berechnen.
- Speichern Sie die Ausgabe von `cksum` in einer Datei, um später die Integrität der Dateien zu überprüfen:
  ```bash
  cksum datei.txt > checksums.txt
  ```
- Vergleichen Sie die Prüfziffern, um sicherzustellen, dass Dateien nicht verändert wurden, indem Sie die Ausgaben von `cksum` für die Original- und die überprüfte Datei vergleichen.