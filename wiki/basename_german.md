# [Linux] Bash basename Verwendung: Extrahiert den Dateinamen aus einem Pfad

## Übersicht
Der `basename`-Befehl in Bash wird verwendet, um den Dateinamen aus einem vollständigen Pfad zu extrahieren. Dies ist besonders nützlich, wenn Sie nur den Namen der Datei ohne den Pfad benötigen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
basename [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Verarbeitet mehrere Argumente und gibt die Basen für jedes Argument zurück.
- `-s`: Entfernt eine angegebene Suffix-Zeichenfolge vom Dateinamen.

## Häufige Beispiele

### Beispiel 1: Einfacher Dateiname
Um den Dateinamen aus einem Pfad zu extrahieren:

```bash
basename /home/user/dokumente/datei.txt
```
**Ausgabe:** `datei.txt`

### Beispiel 2: Mit Suffix entfernen
Um ein Suffix von einem Dateinamen zu entfernen:

```bash
basename /home/user/dokumente/datei.txt .txt
```
**Ausgabe:** `datei`

### Beispiel 3: Mehrere Argumente
Um mehrere Dateinamen auf einmal zu verarbeiten:

```bash
basename -a /home/user/dokumente/datei1.txt /home/user/dokumente/datei2.txt
```
**Ausgabe:**
```
datei1.txt
datei2.txt
```

### Beispiel 4: Suffix für mehrere Dateien entfernen
Um das Suffix `.txt` von mehreren Dateien zu entfernen:

```bash
basename -a /home/user/dokumente/datei1.txt /home/user/dokumente/datei2.txt .txt
```
**Ausgabe:**
```
datei1
datei2
```

## Tipps
- Nutzen Sie `basename` in Skripten, um Dateinamen dynamisch zu verarbeiten.
- Kombinieren Sie `basename` mit anderen Befehlen wie `find`, um gezielt mit Dateinamen zu arbeiten.
- Achten Sie darauf, die Suffix-Option nur zu verwenden, wenn Sie sicher sind, dass die Dateien das angegebene Suffix haben.