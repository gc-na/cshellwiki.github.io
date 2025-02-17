# [Linux] Bash getopts Verwendung: Optionen in Skripten verarbeiten

## Overview
Der Befehl `getopts` wird in Bash-Skripten verwendet, um Optionen und Argumente von der Kommandozeile zu verarbeiten. Er ermöglicht es, benutzerfreundliche Skripte zu erstellen, die Eingaben in Form von Optionen akzeptieren.

## Usage
Die grundlegende Syntax des Befehls `getopts` sieht wie folgt aus:

```bash
getopts optstring variable
```

Hierbei ist `optstring` eine Zeichenkette, die die akzeptierten Optionen definiert, und `variable` ist der Name der Variablen, in der die aktuelle Option gespeichert wird.

## Common Options
- `-a`: Option für eine bestimmte Funktion (benutzerdefiniert).
- `-b`: Eine weitere benutzerdefinierte Option.
- `-c`: Option, die eine bestimmte Aktion ausführt.

## Common Examples

### Beispiel 1: Einfache Optionen
```bash
#!/bin/bash

while getopts "ab" opt; do
  case $opt in
    a)
      echo "Option A aktiviert"
      ;;
    b)
      echo "Option B aktiviert"
      ;;
    *)
      echo "Ungültige Option"
      ;;
  esac
done
```

### Beispiel 2: Optionen mit Argumenten
```bash
#!/bin/bash

while getopts "f:d:" opt; do
  case $opt in
    f)
      echo "Dateiname: $OPTARG"
      ;;
    d)
      echo "Verzeichnis: $OPTARG"
      ;;
    *)
      echo "Ungültige Option"
      ;;
  esac
done
```

### Beispiel 3: Standardoptionen
```bash
#!/bin/bash

while getopts ":ab" opt; do
  case $opt in
    a)
      echo "Option A aktiviert"
      ;;
    b)
      echo "Option B aktiviert"
      ;;
    \?)
      echo "Ungültige Option: -$OPTARG" >&2
      ;;
    :)
      echo "Option -$OPTARG benötigt ein Argument." >&2
      ;;
  esac
done
```

## Tips
- Verwenden Sie ein führendes Doppelpunkt (`:`) in der `optstring`, um anzugeben, dass eine Option ein Argument benötigt.
- Stellen Sie sicher, dass Sie die Optionen in einer `case`-Anweisung behandeln, um die Lesbarkeit und Wartbarkeit Ihres Skripts zu verbessern.
- Testen Sie Ihr Skript mit verschiedenen Kombinationen von Optionen, um sicherzustellen, dass alle möglichen Eingaben korrekt verarbeitet werden.