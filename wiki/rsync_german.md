# [Linux] Bash rsync Verwendung: Dateien synchronisieren und übertragen

## Übersicht
Der `rsync`-Befehl ist ein leistungsstarkes Tool zur Synchronisierung und Übertragung von Dateien und Verzeichnissen zwischen verschiedenen Standorten. Es ist besonders nützlich, um Daten effizient zu sichern oder zu kopieren, da es nur die Änderungen überträgt und so Bandbreite spart.

## Verwendung
Die grundlegende Syntax des `rsync`-Befehls lautet:

```bash
rsync [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
Hier sind einige gängige Optionen, die mit `rsync` verwendet werden können:

- `-a`: Archivmodus; kopiert Dateien rekursiv und bewahrt die Dateiberechtigungen.
- `-v`: Ausführliche Ausgabe; zeigt den Fortschritt der Übertragung an.
- `-z`: Komprimiert die Daten während der Übertragung, um Bandbreite zu sparen.
- `-r`: Rekursive Übertragung von Verzeichnissen.
- `--delete`: Löscht Dateien im Ziel, die nicht mehr im Quellverzeichnis vorhanden sind.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `rsync`:

1. **Ein einfaches Backup eines Verzeichnisses:**
   ```bash
   rsync -av /pfad/zum/quellverzeichnis/ /pfad/zum/zielverzeichnis/
   ```

2. **Datenübertragung mit Kompression:**
   ```bash
   rsync -avz /pfad/zum/quellverzeichnis/ benutzer@remote:/pfad/zum/zielverzeichnis/
   ```

3. **Synchronisieren mit Löschen von nicht mehr vorhandenen Dateien:**
   ```bash
   rsync -av --delete /pfad/zum/quellverzeichnis/ /pfad/zum/zielverzeichnis/
   ```

4. **Übertragung über SSH:**
   ```bash
   rsync -avz -e ssh /pfad/zum/quellverzeichnis/ benutzer@remote:/pfad/zum/zielverzeichnis/
   ```

## Tipps
- Verwenden Sie die Option `-n` (Trockenlauf), um zu sehen, welche Dateien übertragen werden, ohne tatsächlich Änderungen vorzunehmen:
  ```bash
  rsync -avn /pfad/zum/quellverzeichnis/ /pfad/zum/zielverzeichnis/
  ```

- Achten Sie darauf, einen abschließenden Schrägstrich (`/`) im Quellverzeichnis zu verwenden, um nur den Inhalt und nicht das Verzeichnis selbst zu kopieren.

- Nutzen Sie `--progress`, um den Fortschritt der Übertragung in Echtzeit zu verfolgen:
  ```bash
  rsync -av --progress /pfad/zum/quellverzeichnis/ /pfad/zum/zielverzeichnis/
  ``` 

Mit diesen Informationen sind Sie gut gerüstet, um `rsync` effektiv für Ihre Dateiübertragungen und -synchronisierungen zu nutzen.