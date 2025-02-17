# [Linux] Bash pwd Verwendung: Gibt das aktuelle Verzeichnis aus

## Übersicht
Der Befehl `pwd` (print working directory) wird in der Bash verwendet, um das aktuelle Arbeitsverzeichnis anzuzeigen. Es ist ein einfaches, aber nützliches Werkzeug, um den Pfad des Verzeichnisses zu ermitteln, in dem Sie sich gerade befinden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
pwd [Optionen]
```

## Häufige Optionen
- `-L`: Gibt den logischen Pfad des aktuellen Verzeichnisses aus (Standardverhalten).
- `-P`: Gibt den physischen Pfad des aktuellen Verzeichnisses aus, wobei symbolische Links aufgelöst werden.

## Häufige Beispiele
1. **Einfaches Anzeigen des aktuellen Verzeichnisses:**
   ```bash
   pwd
   ```

2. **Anzeigen des physischen Pfades:**
   ```bash
   pwd -P
   ```

3. **Anzeigen des logischen Pfades (Standardverhalten):**
   ```bash
   pwd -L
   ```

## Tipps
- Verwenden Sie `pwd` regelmäßig, um sicherzustellen, dass Sie sich im richtigen Verzeichnis befinden, insbesondere wenn Sie mit mehreren Verzeichnissen arbeiten.
- Kombinieren Sie `pwd` mit anderen Befehlen, um Skripte zu erstellen, die den aktuellen Pfad dynamisch verwenden.