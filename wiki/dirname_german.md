# [Unix] C Shell (csh) dirname Verwendung: Gibt das Verzeichnis eines Pfades zurück

## Übersicht
Der Befehl `dirname` wird verwendet, um den Verzeichnispfad eines gegebenen Dateipfades zu extrahieren. Er entfernt den Dateinamen und gibt nur den übergeordneten Verzeichnisnamen zurück.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
dirname [Optionen] [Argumente]
```

## Häufige Optionen
- **Keine speziellen Optionen**: Der Befehl `dirname` hat keine speziellen Optionen. Er wird in der Regel mit einem oder mehreren Argumenten verwendet, die die Pfade darstellen.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des Befehls `dirname`:

1. **Einfacher Verzeichnispfad**
   ```csh
   dirname /usr/local/bin/script.sh
   ```
   Ausgabe:
   ```
   /usr/local/bin
   ```

2. **Verzeichnispfad ohne Dateiendung**
   ```csh
   dirname /home/user/documents/report.pdf
   ```
   Ausgabe:
   ```
   /home/user/documents
   ```

3. **Mehrere Argumente**
   ```csh
   dirname /var/log/syslog /etc/hosts
   ```
   Ausgabe:
   ```
   /var/log
   /etc
   ```

4. **Verzeichnispfad eines relativen Pfades**
   ```csh
   dirname ./myfolder/myfile.txt
   ```
   Ausgabe:
   ```
   ./myfolder
   ```

## Tipps
- Verwenden Sie `dirname` in Skripten, um den Verzeichnispfad dynamisch zu extrahieren, wenn Sie mit Dateipfaden arbeiten.
- Kombinieren Sie `dirname` mit anderen Befehlen wie `basename`, um sowohl den Verzeichnispfad als auch den Dateinamen zu erhalten.
- Achten Sie darauf, dass `dirname` nur den Verzeichnispfad zurückgibt; es entfernt keine führenden oder nachfolgenden Leerzeichen.