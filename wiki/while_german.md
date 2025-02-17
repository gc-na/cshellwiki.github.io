# [Linux] Bash while Verwendung: Schleifensteuerung in Bash

## Übersicht
Der `while`-Befehl in Bash wird verwendet, um eine Schleife zu erstellen, die eine bestimmte Bedingung überprüft. Solange die Bedingung wahr ist, wird der enthaltene Codeblock wiederholt ausgeführt. Dies ist nützlich für Aufgaben, die wiederholt ausgeführt werden müssen, bis ein bestimmter Zustand erreicht ist.

## Verwendung
Die grundlegende Syntax des `while`-Befehls sieht folgendermaßen aus:

```bash
while [Bedingung]; do
    # Befehle
done
```

## Häufige Optionen
- **Bedingung**: Ein Ausdruck, der wahr oder falsch sein kann. Die Schleife wird fortgesetzt, solange dieser Ausdruck wahr ist.
- **do**: Leitet den Block von Befehlen ein, die wiederholt ausgeführt werden sollen.
- **done**: Beendet den `while`-Block.

## Häufige Beispiele

### Beispiel 1: Zählen von 1 bis 5
```bash
count=1
while [ $count -le 5 ]; do
    echo "Zahl: $count"
    ((count++))
done
```

### Beispiel 2: Benutzereingabe abfragen
```bash
input=""
while [ "$input" != "exit" ]; do
    read -p "Geben Sie etwas ein (exit zum Beenden): " input
    echo "Sie haben eingegeben: $input"
done
```

### Beispiel 3: Dateien in einem Verzeichnis auflisten
```bash
files=(*)
index=0
while [ $index -lt ${#files[@]} ]; do
    echo "Datei: ${files[$index]}"
    ((index++))
done
```

## Tipps
- Achten Sie darauf, dass die Bedingung irgendwann falsch wird, um eine Endlosschleife zu vermeiden.
- Verwenden Sie `break`, um die Schleife vorzeitig zu beenden, wenn eine bestimmte Bedingung erfüllt ist.
- Nutzen Sie `sleep`, um die Ausführung innerhalb der Schleife zu verzögern, falls nötig, um die Systemressourcen zu schonen.