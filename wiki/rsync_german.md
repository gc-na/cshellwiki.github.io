# [Linux] C Shell (csh) rsync Verwendung: Dateien synchronisieren und übertragen

## Übersicht
Der `rsync`-Befehl wird verwendet, um Dateien und Verzeichnisse zwischen verschiedenen Standorten zu synchronisieren und zu übertragen. Er ist besonders nützlich, um nur die Änderungen zu übertragen, was die Übertragungszeit und den Bandbreitenverbrauch reduziert.

## Verwendung
Die grundlegende Syntax des `rsync`-Befehls lautet:

```bash
rsync [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
- `-a`: Aktiviert den Archivmodus, der rekursive Übertragungen und die Erhaltung von Berechtigungen, Zeitstempeln und Symbolischen Links ermöglicht.
- `-v`: Aktiviert die ausführliche Ausgabe, um den Fortschritt der Übertragung anzuzeigen.
- `-z`: Komprimiert die Daten während der Übertragung, um die Bandbreite zu sparen.
- `-r`: Überträgt Verzeichnisse rekursiv.
- `--delete`: Löscht Dateien im Zielverzeichnis, die nicht mehr im Quellverzeichnis vorhanden sind.

## Häufige Beispiele
1. **Ein einfaches Synchronisieren von Dateien:**
   ```bash
   rsync -av /pfad/zum/quellverzeichnis/ /pfad/zum/zielverzeichnis/
   ```

2. **Synchronisieren mit Kompression:**
   ```bash
   rsync -avz /pfad/zum/quellverzeichnis/ user@remote:/pfad/zum/zielverzeichnis/
   ```

3. **Synchronisieren und Löschen nicht mehr vorhandener Dateien:**
   ```bash
   rsync -av --delete /pfad/zum/quellverzeichnis/ /pfad/zum/zielverzeichnis/
   ```

4. **Nur bestimmte Dateitypen synchronisieren:**
   ```bash
   rsync -av --include='*.jpg' --exclude='*' /pfad/zum/quellverzeichnis/ /pfad/zum/zielverzeichnis/
   ```

## Tipps
- Verwenden Sie `--dry-run`, um zu sehen, welche Änderungen vorgenommen werden, ohne tatsächlich Dateien zu übertragen.
- Stellen Sie sicher, dass Sie die Trailing Slash (`/`) im Quellverzeichnis korrekt verwenden, um die gewünschten Ergebnisse zu erzielen.
- Nutzen Sie `rsync` über SSH für sichere Übertragungen, indem Sie `user@remote:/pfad/zum/zielverzeichnis/` angeben.