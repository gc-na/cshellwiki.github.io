# [Linux] Bash pr: Textdateien formatieren und drucken

## Übersicht
Der `pr` Befehl wird verwendet, um Textdateien für den Druck zu formatieren. Er teilt den Inhalt einer Datei in mehrere Spalten und fügt Kopfzeilen sowie Seitenumbrüche hinzu, was die Lesbarkeit beim Drucken verbessert.

## Verwendung
Die grundlegende Syntax des `pr` Befehls lautet:

```bash
pr [Optionen] [Argumente]
```

## Häufige Optionen
- `-h, --header=TEXT`: Fügt eine benutzerdefinierte Kopfzeile hinzu.
- `-l, --length=NUM`: Legt die Seitenlänge in Zeilen fest.
- `-n, --number`: Nummeriert die Ausgaben.
- `-t, --omit-header`: Unterdrückt die Kopfzeile.
- `-s, --separator=STRING`: Legt den Trennzeichen für Spalten fest.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `pr` Befehls:

1. **Einfaches Formatieren einer Datei:**
   ```bash
   pr datei.txt
   ```

2. **Formatieren mit benutzerdefinierter Kopfzeile:**
   ```bash
   pr -h "Mein Dokument" datei.txt
   ```

3. **Ausgabe in zwei Spalten:**
   ```bash
   pr -2 datei.txt
   ```

4. **Nummerierte Ausgabe:**
   ```bash
   pr -n datei.txt
   ```

5. **Seitenlänge auf 40 Zeilen festlegen:**
   ```bash
   pr -l 40 datei.txt
   ```

## Tipps
- Verwenden Sie die Option `-t`, wenn Sie die Kopfzeile nicht benötigen, um Platz zu sparen.
- Experimentieren Sie mit der Spaltenanzahl, um die Lesbarkeit je nach Inhalt zu optimieren.
- Nutzen Sie die Nummerierungsoption, um die Referenzierung in langen Dokumenten zu erleichtern.