# [Linux] C Shell (csh) sed Verwendung: Textbearbeitung im Stream

## Übersicht
Der `sed`-Befehl (Stream Editor) ist ein leistungsstarkes Tool zur Bearbeitung von Textströmen. Er wird häufig verwendet, um Text in Dateien oder von der Standardeingabe zu suchen, zu ersetzen, zu löschen oder zu formatieren.

## Verwendung
Die grundlegende Syntax des `sed`-Befehls lautet:

```bash
sed [Optionen] [Argumente]
```

## Häufige Optionen
- `-e`: Ermöglicht das Angeben mehrerer Bearbeitungsanweisungen.
- `-f`: Liest Bearbeitungsanweisungen aus einer Datei.
- `-i`: Führt die Bearbeitung direkt in der Datei durch (in-place).
- `-n`: Unterdrückt die Standardausgabe; nützlich in Kombination mit `p` (print).
- `s`: Steht für "substitute" und wird verwendet, um Text zu ersetzen.

## Häufige Beispiele

### Beispiel 1: Text ersetzen
Um alle Vorkommen von "alt" durch "neu" in einer Datei zu ersetzen:

```bash
sed 's/alt/neu/g' datei.txt
```

### Beispiel 2: Zeilen löschen
Um alle Zeilen zu löschen, die das Wort "entfernen" enthalten:

```bash
sed '/entfernen/d' datei.txt
```

### Beispiel 3: In-place Bearbeitung
Um "alt" durch "neu" in der Datei direkt zu ersetzen:

```bash
sed -i 's/alt/neu/g' datei.txt
```

### Beispiel 4: Mehrere Bearbeitungen
Um mehrere Ersetzungen in einer Datei durchzuführen:

```bash
sed -e 's/alt/neu/g' -e 's/alt2/neu2/g' datei.txt
```

### Beispiel 5: Nur bestimmte Zeilen anzeigen
Um nur die Zeilen anzuzeigen, die das Wort "anzeigen" enthalten:

```bash
sed -n '/anzeigen/p' datei.txt
```

## Tipps
- Verwenden Sie die `-i`-Option mit Bedacht, da sie die Originaldatei überschreibt. Es ist ratsam, vorher eine Sicherungskopie zu erstellen.
- Testen Sie Ihre `sed`-Befehle zuerst ohne die `-i`-Option, um sicherzustellen, dass die Ausgabe wie gewünscht ist.
- Nutzen Sie reguläre Ausdrücke für komplexere Such- und Ersetzungsoperationen, um die Flexibilität von `sed` voll auszuschöpfen.