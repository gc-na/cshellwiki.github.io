# [Linux] Bash test Verwendung: Überprüfen von Bedingungen

## Übersicht
Der `test` Befehl in Bash wird verwendet, um Bedingungen zu überprüfen. Er gibt einen Statuscode zurück, der angibt, ob die getestete Bedingung wahr oder falsch ist. Dies ist besonders nützlich in Skripten, um Entscheidungen zu treffen.

## Verwendung
Die grundlegende Syntax des `test` Befehls lautet:

```bash
test [Optionen] [Argumente]
```

## Häufige Optionen
- `-e DATEI`: Überprüft, ob die angegebene Datei existiert.
- `-d DATEI`: Überprüft, ob die angegebene Datei ein Verzeichnis ist.
- `-f DATEI`: Überprüft, ob die angegebene Datei eine reguläre Datei ist.
- `-z STRING`: Überprüft, ob die angegebene Zeichenkette leer ist.
- `-n STRING`: Überprüft, ob die angegebene Zeichenkette nicht leer ist.
- `NUM1 -eq NUM2`: Überprüft, ob zwei Zahlen gleich sind.
- `NUM1 -ne NUM2`: Überprüft, ob zwei Zahlen ungleich sind.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `test` Befehls:

### Beispiel 1: Überprüfen, ob eine Datei existiert
```bash
if test -e meine_datei.txt; then
    echo "Die Datei existiert."
else
    echo "Die Datei existiert nicht."
fi
```

### Beispiel 2: Überprüfen, ob ein Verzeichnis vorhanden ist
```bash
if test -d /mein/verzeichnis; then
    echo "Das Verzeichnis existiert."
else
    echo "Das Verzeichnis existiert nicht."
fi
```

### Beispiel 3: Überprüfen, ob eine Zeichenkette leer ist
```bash
meine_variable=""
if test -z "$meine_variable"; then
    echo "Die Variable ist leer."
else
    echo "Die Variable ist nicht leer."
fi
```

### Beispiel 4: Zahlenvergleich
```bash
zahl1=10
zahl2=20
if test $zahl1 -lt $zahl2; then
    echo "$zahl1 ist kleiner als $zahl2."
else
    echo "$zahl1 ist nicht kleiner als $zahl2."
fi
```

## Tipps
- Verwenden Sie die `[[` und `]]` Syntax anstelle von `test`, um die Lesbarkeit zu verbessern und erweiterte Funktionen zu nutzen.
- Kombinieren Sie Bedingungen mit `-a` (und) oder `-o` (oder) für komplexere Tests.
- Achten Sie darauf, Leerzeichen um die Operatoren zu setzen, um Syntaxfehler zu vermeiden.