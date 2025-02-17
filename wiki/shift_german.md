# [Linux] Bash shift Verwendung: Verschiebt Positionsparameter nach links

## Übersicht
Der `shift` Befehl in Bash wird verwendet, um die Positionsparameter in einem Shell-Skript oder einer Funktion nach links zu verschieben. Dies bedeutet, dass der erste Parameter `$1` entfernt wird und alle nachfolgenden Parameter um eins nach vorne verschoben werden. Dies ist besonders nützlich, wenn Sie mit einer variablen Anzahl von Argumenten arbeiten und diese nacheinander verarbeiten möchten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
shift [n]
```

Hierbei ist `n` die Anzahl der Positionen, um die die Parameter verschoben werden sollen. Wenn `n` nicht angegeben ist, wird standardmäßig um eins verschoben.

## Häufige Optionen
- `n`: Gibt die Anzahl der Positionen an, um die die Parameter verschoben werden sollen. Standardmäßig wird um eins verschoben.

## Häufige Beispiele

### Beispiel 1: Einfaches Verschieben
```bash
#!/bin/bash
set -- "Erster" "Zweiter" "Dritter"
echo "Vor shift: $1 $2 $3"
shift
echo "Nach shift: $1 $2 $3"
```
**Ausgabe:**
```
Vor shift: Erster Zweiter Dritter
Nach shift: Zweiter Dritter
```

### Beispiel 2: Mehrere Parameter verschieben
```bash
#!/bin/bash
set -- "Eins" "Zwei" "Drei" "Vier"
echo "Vor shift: $1 $2 $3 $4"
shift 2
echo "Nach shift: $1 $2"
```
**Ausgabe:**
```
Vor shift: Eins Zwei Drei Vier
Nach shift: Drei Vier
```

### Beispiel 3: In einer Schleife
```bash
#!/bin/bash
set -- "Apfel" "Banane" "Kirsche"
while [ "$#" -gt 0 ]; do
    echo "Frucht: $1"
    shift
done
```
**Ausgabe:**
```
Frucht: Apfel
Frucht: Banane
Frucht: Kirsche
```

## Tipps
- Verwenden Sie `shift` in Schleifen, um alle übergebenen Argumente nacheinander zu verarbeiten.
- Achten Sie darauf, dass nach dem Verschieben von Parametern die Anzahl der verbleibenden Parameter (`$#`) abnimmt. Überprüfen Sie dies gegebenenfalls, um Fehler zu vermeiden.
- Kombinieren Sie `shift` mit anderen Befehlen wie `getopts`, um Optionen in Skripten effizient zu verarbeiten.