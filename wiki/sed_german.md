# [Linux] Bash sed Verwendung: Textbearbeitung im Stream

## Übersicht
Der `sed`-Befehl (Stream Editor) ist ein leistungsstarkes Tool in der Bash, das verwendet wird, um Text in einem Datenstrom zu bearbeiten. Er ermöglicht das Suchen, Ersetzen, Einfügen und Löschen von Text in Dateien oder von Eingabeströmen.

## Verwendung
Die grundlegende Syntax des `sed`-Befehls lautet:

```bash
sed [Optionen] [Argumente]
```

## Häufige Optionen
- `-e`: Ermöglicht das Ausführen mehrerer Befehle.
- `-i`: Ändert die Datei direkt (in-place).
- `-n`: Unterdrückt die Ausgabe von Zeilen, die nicht bearbeitet wurden.
- `s`: Steht für den Ersetzungsbefehl (substitute).

## Häufige Beispiele

### 1. Text ersetzen
Um ein Wort in einer Datei zu ersetzen, verwenden Sie den folgenden Befehl:

```bash
sed 's/alt/neu/' datei.txt
```

Dieser Befehl ersetzt das erste Vorkommen von "alt" durch "neu" in jeder Zeile von `datei.txt`.

### 2. Text in einer Datei direkt ändern
Um die Datei direkt zu ändern, können Sie die `-i`-Option verwenden:

```bash
sed -i 's/alt/neu/g' datei.txt
```

Hier wird jedes Vorkommen von "alt" durch "neu" ersetzt.

### 3. Zeilen löschen
Um alle Zeilen zu löschen, die ein bestimmtes Wort enthalten, verwenden Sie:

```bash
sed '/unwichtig/d' datei.txt
```

Dieser Befehl entfernt alle Zeilen, die "unwichtig" enthalten.

### 4. Mehrere Ersetzungen
Um mehrere Ersetzungen in einem Befehl durchzuführen, verwenden Sie die `-e`-Option:

```bash
sed -e 's/alt/neu/' -e 's/weit/nah/' datei.txt
```

Hier werden sowohl "alt" durch "neu" als auch "weit" durch "nah" ersetzt.

## Tipps
- Verwenden Sie die `-n`-Option, wenn Sie nur bestimmte Zeilen ausgeben möchten, die mit einem bestimmten Muster übereinstimmen.
- Machen Sie vor der Verwendung der `-i`-Option eine Sicherungskopie Ihrer Datei, um Datenverlust zu vermeiden.
- Testen Sie Ihre `sed`-Befehle zuerst ohne die `-i`-Option, um sicherzustellen, dass die Ausgabe wie gewünscht ist.