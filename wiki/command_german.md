# [Linux] Bash-Befehl grep: Text in Dateien durchsuchen

## Übersicht
Der Befehl `grep` wird verwendet, um nach bestimmten Mustern in Textdateien zu suchen. Er ist besonders nützlich, um Zeilen zu finden, die einen bestimmten Text enthalten, und kann mit regulären Ausdrücken arbeiten, um komplexere Suchmuster zu ermöglichen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
grep [Optionen] Muster [Dateien]
```

## Häufige Optionen
- `-i`: Ignoriere Groß- und Kleinschreibung bei der Suche.
- `-v`: Zeige nur die Zeilen an, die **nicht** dem Muster entsprechen.
- `-r`: Durchsuche Verzeichnisse rekursiv.
- `-n`: Zeige die Zeilennummern der gefundenen Übereinstimmungen an.
- `-l`: Zeige nur die Namen der Dateien an, die das Muster enthalten.

## Häufige Beispiele
1. **Einfaches Suchen nach einem Wort in einer Datei:**
   ```bash
   grep "Suchbegriff" datei.txt
   ```

2. **Suchen ohne Berücksichtigung der Groß- und Kleinschreibung:**
   ```bash
   grep -i "suchbegriff" datei.txt
   ```

3. **Zeilen anzeigen, die nicht dem Muster entsprechen:**
   ```bash
   grep -v "Suchbegriff" datei.txt
   ```

4. **Rekursive Suche in einem Verzeichnis:**
   ```bash
   grep -r "Suchbegriff" /pfad/zum/verzeichnis
   ```

5. **Zeilennummern der gefundenen Übereinstimmungen anzeigen:**
   ```bash
   grep -n "Suchbegriff" datei.txt
   ```

## Tipps
- Verwende die Option `-r`, um schnell in vielen Dateien innerhalb eines Verzeichnisses nach einem Muster zu suchen.
- Kombiniere `grep` mit anderen Befehlen wie `cat` oder `find`, um die Suche zu verfeinern.
- Nutze reguläre Ausdrücke, um komplexere Suchmuster zu erstellen, z.B. `grep "^A.*Z"` um Zeilen zu finden, die mit "A" beginnen und mit "Z" enden.