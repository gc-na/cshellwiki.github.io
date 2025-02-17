# [Linux] Bash du Verwendung: Speicherplatznutzung anzeigen

## Übersicht
Der `du` (Disk Usage) Befehl wird verwendet, um den Speicherplatzverbrauch von Dateien und Verzeichnissen im Dateisystem anzuzeigen. Er hilft Benutzern, den Platzbedarf zu analysieren und zu verstehen, welche Dateien oder Ordner den meisten Speicherplatz beanspruchen.

## Verwendung
Die grundlegende Syntax des `du` Befehls lautet:

```bash
du [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Gibt die Größe in menschenlesbarem Format aus (z.B. KB, MB, GB).
- `-s`: Zeigt nur die Gesamtgröße für jedes angegebene Argument an.
- `-a`: Zeigt die Größe aller Dateien und Verzeichnisse an, nicht nur der Verzeichnisse.
- `-c`: Gibt eine Gesamtsumme für alle angegebenen Argumente aus.
- `--max-depth=N`: Beschränkt die Ausgabe auf N Ebenen von Unterverzeichnissen.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `du` Befehls:

1. **Gesamten Speicherplatz eines Verzeichnisses anzeigen:**
   ```bash
   du /pfad/zum/verzeichnis
   ```

2. **Größen in menschenlesbarem Format anzeigen:**
   ```bash
   du -h /pfad/zum/verzeichnis
   ```

3. **Nur die Gesamtgröße eines Verzeichnisses anzeigen:**
   ```bash
   du -sh /pfad/zum/verzeichnis
   ```

4. **Größen aller Dateien und Verzeichnisse im aktuellen Verzeichnis anzeigen:**
   ```bash
   du -ah .
   ```

5. **Größen mit einer maximalen Tiefe von 1 anzeigen:**
   ```bash
   du --max-depth=1 -h /pfad/zum/verzeichnis
   ```

## Tipps
- Verwenden Sie die `-h` Option, um die Ausgabe leichter lesbar zu machen.
- Kombinieren Sie `du` mit `sort`, um die größten Verzeichnisse oder Dateien anzuzeigen:
  ```bash
  du -ah /pfad/zum/verzeichnis | sort -rh | head -n 10
  ```
- Nutzen Sie `-c`, um eine Gesamtsumme für mehrere Verzeichnisse zu erhalten:
  ```bash
  du -ch /pfad/zum/verzeichnis1 /pfad/zum/verzeichnis2
  ```