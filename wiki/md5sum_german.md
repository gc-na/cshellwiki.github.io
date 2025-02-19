# [Linux] C Shell (csh) md5sum Verwendung: Berechnung von MD5-Prüfziffern

## Übersicht
Der Befehl `md5sum` wird verwendet, um die MD5-Prüfziffer (Checksum) einer Datei zu berechnen. Diese Prüfziffer dient dazu, die Integrität von Dateien zu überprüfen, indem sie sicherstellt, dass der Inhalt einer Datei nicht verändert wurde.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
md5sum [Optionen] [Argumente]
```

## Häufige Optionen
- `-b`: Berechnet die Prüfziffer für Binärdateien.
- `-c`: Überprüft die Prüfziffern von Dateien anhand einer Prüfziffernliste.
- `-t`: Berechnet die Prüfziffer für Textdateien.
- `--help`: Zeigt eine Hilfeseite mit Informationen zu den verfügbaren Optionen an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `md5sum`:

1. **Berechnung der MD5-Prüfziffer einer Datei:**

   ```csh
   md5sum datei.txt
   ```

2. **Berechnung der MD5-Prüfziffer für mehrere Dateien:**

   ```csh
   md5sum datei1.txt datei2.txt
   ```

3. **Überprüfung der Prüfziffern anhand einer Liste:**

   Zuerst erstellen Sie eine Prüfziffernliste:

   ```csh
   md5sum datei.txt > checksums.md5
   ```

   Dann überprüfen Sie die Prüfziffern:

   ```csh
   md5sum -c checksums.md5
   ```

4. **Berechnung der Prüfziffer für eine Binärdatei:**

   ```csh
   md5sum -b bild.png
   ```

## Tipps
- Verwenden Sie `md5sum` in Kombination mit `-c`, um sicherzustellen, dass Dateien nicht verändert wurden, insbesondere bei wichtigen Daten.
- Speichern Sie Prüfziffern in einer Datei, um die Integrität von Downloads oder Backups zu überprüfen.
- Beachten Sie, dass MD5 nicht als sicher gilt für kryptografische Zwecke, verwenden Sie es daher nur zur Integritätsprüfung.