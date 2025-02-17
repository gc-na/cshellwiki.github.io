# [Linux] Bash continue Verwendung: Fortsetzen einer Schleife

## Übersicht
Der Befehl `continue` wird in Bash verwendet, um die aktuelle Iteration einer Schleife zu beenden und mit der nächsten Iteration fortzufahren. Dies ist besonders nützlich, wenn bestimmte Bedingungen erfüllt sind und der Rest des Schleifenblocks übersprungen werden soll.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
continue [N]
```

Hierbei steht `N` für die Anzahl der Schleifen, die übersprungen werden sollen. Wenn `N` nicht angegeben ist, wird die nächste Iteration der innersten Schleife fortgesetzt.

## Häufige Optionen
- `N`: Gibt an, wie viele Schleifen übersprungen werden sollen. Standardmäßig wird nur die nächste Iteration übersprungen.

## Häufige Beispiele

### Beispiel 1: Einfache Schleife mit continue
In diesem Beispiel wird eine Schleife verwendet, die die Zahlen von 1 bis 5 durchläuft. Wenn die Zahl 3 erreicht wird, wird die Iteration übersprungen.

```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        continue
    fi
    echo $i
done
```
**Ausgabe:**
```
1
2
4
5
```

### Beispiel 2: continue in einer while-Schleife
Hier wird `continue` in einer `while`-Schleife verwendet, um gerade Zahlen zu überspringen.

```bash
i=1
while [ $i -le 5 ]; do
    if [ $((i % 2)) -eq 0 ]; then
        ((i++))
        continue
    fi
    echo $i
    ((i++))
done
```
**Ausgabe:**
```
1
3
5
```

### Beispiel 3: Verwendung von continue mit N
In diesem Beispiel wird `continue` verwendet, um die nächste Iteration einer äußeren Schleife zu überspringen.

```bash
for i in {1..3}; do
    for j in {1..3}; do
        if [ $j -eq 2 ]; then
            continue 2
        fi
        echo "i=$i, j=$j"
    done
done
```
**Ausgabe:**
```
i=1, j=1
i=1, j=3
i=2, j=1
i=2, j=3
i=3, j=1
i=3, j=3
```

## Tipps
- Verwenden Sie `continue`, um den Code lesbarer zu machen, indem Sie unnötige Verschachtelungen vermeiden.
- Achten Sie darauf, dass `continue` nur in Schleifen verwendet wird; außerhalb einer Schleife führt es zu einem Fehler.
- Testen Sie Ihre Bedingungen gründlich, um sicherzustellen, dass die Schleife wie gewünscht funktioniert.