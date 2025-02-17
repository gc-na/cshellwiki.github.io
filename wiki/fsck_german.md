# [Linux] Bash fsck Verwendung: Überprüfen und Reparieren von Dateisystemen

## Übersicht
Der Befehl `fsck` (File System Consistency Check) wird verwendet, um die Integrität von Dateisystemen zu überprüfen und gegebenenfalls zu reparieren. Er ist ein wichtiges Werkzeug zur Wartung von Dateisystemen in Unix-ähnlichen Betriebssystemen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
fsck [Optionen] [Argumente]
```

## Häufige Optionen
- `-A`: Überprüft alle Dateisysteme in der `/etc/fstab`-Datei.
- `-N`: Zeigt an, was `fsck` tun würde, ohne tatsächlich Änderungen vorzunehmen.
- `-y`: Bestätigt automatisch alle Reparaturen, die `fsck` vorschlägt.
- `-f`: Erzwingt die Überprüfung eines Dateisystems, auch wenn es als sauber markiert ist.
- `-C`: Gibt den Fortschritt in einer Datei aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `fsck`:

1. Überprüfen eines bestimmten Dateisystems:
   ```bash
   fsck /dev/sda1
   ```

2. Überprüfen aller Dateisysteme in der `/etc/fstab`-Datei:
   ```bash
   fsck -A
   ```

3. Automatisches Bestätigen aller Reparaturen:
   ```bash
   fsck -y /dev/sda1
   ```

4. Erzwingen der Überprüfung eines Dateisystems:
   ```bash
   fsck -f /dev/sda1
   ```

5. Nur eine Simulation der Überprüfung durchführen:
   ```bash
   fsck -N /dev/sda1
   ```

## Tipps
- Führen Sie `fsck` immer im Einzelbenutzermodus oder von einem Live-System aus, um Probleme mit gemounteten Dateisystemen zu vermeiden.
- Sichern Sie wichtige Daten, bevor Sie `fsck` ausführen, insbesondere wenn Sie Reparaturen durchführen.
- Verwenden Sie die Option `-y` mit Bedacht, da dies alle vorgeschlagenen Reparaturen automatisch akzeptiert.