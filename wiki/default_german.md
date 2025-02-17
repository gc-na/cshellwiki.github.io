# [Linux] Bash standardbefehl `ls`: Dateien und Verzeichnisse auflisten

## Übersicht
Der Befehl `ls` wird verwendet, um Dateien und Verzeichnisse in einem Verzeichnis aufzulisten. Er zeigt eine Übersicht der Inhalte eines Verzeichnisses an und bietet verschiedene Optionen zur Anpassung der Anzeige.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
ls [Optionen] [Argumente]
```

## Häufige Optionen
- `-l`: Listet die Dateien in einem detaillierten Format auf, einschließlich Berechtigungen, Besitzer, Größe und Änderungsdatum.
- `-a`: Zeigt auch versteckte Dateien an (Dateien, die mit einem Punkt beginnen).
- `-h`: Gibt die Dateigrößen in einem menschenlesbaren Format aus (z. B. KB, MB).
- `-R`: Listet die Inhalte von Verzeichnissen rekursiv auf.
- `-t`: Sortiert die Dateien nach Änderungsdatum, wobei die neuesten Dateien zuerst angezeigt werden.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des Befehls `ls`:

1. **Einfaches Auflisten von Dateien:**
   ```bash
   ls
   ```

2. **Auflisten aller Dateien, einschließlich versteckter:**
   ```bash
   ls -a
   ```

3. **Detaillierte Auflistung der Dateien:**
   ```bash
   ls -l
   ```

4. **Detaillierte Auflistung mit menschenlesbaren Größen:**
   ```bash
   ls -lh
   ```

5. **Rekursives Auflisten von Verzeichnissen:**
   ```bash
   ls -R
   ```

6. **Auflisten von Dateien, sortiert nach Änderungsdatum:**
   ```bash
   ls -lt
   ```

## Tipps
- Verwenden Sie `ls -lah`, um eine umfassende und leicht lesbare Übersicht über alle Dateien, einschließlich versteckter, zu erhalten.
- Kombinieren Sie Optionen, um die Anzeige nach Ihren Bedürfnissen anzupassen, z. B. `ls -lR` für eine detaillierte, rekursive Auflistung.
- Nutzen Sie die Tabulator-Taste, um die Autovervollständigung zu verwenden, wenn Sie Verzeichnisse oder Dateinamen eingeben.