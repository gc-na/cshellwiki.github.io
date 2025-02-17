# [Linux] Bash if Verwendung: Bedingte Ausführung von Befehlen

## Overview
Der `if`-Befehl in Bash ermöglicht es, bedingte Anweisungen auszuführen. Er prüft, ob eine bestimmte Bedingung erfüllt ist, und führt dann den entsprechenden Codeblock aus. Dies ist besonders nützlich in Skripten, um Entscheidungen basierend auf bestimmten Kriterien zu treffen.

## Usage
Die grundlegende Syntax des `if`-Befehls sieht folgendermaßen aus:

```bash
if [ Bedingung ]; then
    # Befehle, die ausgeführt werden, wenn die Bedingung wahr ist
fi
```

## Common Options
- `-e`: Überprüft, ob eine Datei existiert.
- `-d`: Überprüft, ob ein Verzeichnis existiert.
- `-f`: Überprüft, ob eine Datei eine reguläre Datei ist.
- `-z`: Überprüft, ob eine Zeichenkette leer ist.

## Common Examples

### Beispiel 1: Überprüfen, ob eine Datei existiert
```bash
if [ -e "meine_datei.txt" ]; then
    echo "Die Datei existiert."
else
    echo "Die Datei existiert nicht."
fi
```

### Beispiel 2: Überprüfen, ob ein Verzeichnis existiert
```bash
if [ -d "/mein/verzeichnis" ]; then
    echo "Das Verzeichnis existiert."
else
    echo "Das Verzeichnis existiert nicht."
fi
```

### Beispiel 3: Überprüfen, ob eine Variable leer ist
```bash
meine_variable=""
if [ -z "$meine_variable" ]; then
    echo "Die Variable ist leer."
else
    echo "Die Variable hat einen Wert."
fi
```

### Beispiel 4: Vergleichen von Zahlen
```bash
zahl1=10
zahl2=20
if [ $zahl1 -lt $zahl2 ]; then
    echo "$zahl1 ist kleiner als $zahl2."
else
    echo "$zahl1 ist nicht kleiner als $zahl2."
fi
```

## Tips
- Achte darauf, Leerzeichen um die eckigen Klammern zu setzen, da dies für die korrekte Syntax wichtig ist.
- Verwende `elif`, um mehrere Bedingungen zu überprüfen.
- Schließe immer den `fi`-Befehl ab, um die `if`-Anweisung zu beenden.