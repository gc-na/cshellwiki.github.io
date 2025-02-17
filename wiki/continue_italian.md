# [Linux] Bash continue uso: Consente di riprendere l'esecuzione di un ciclo

## Overview
Il comando `continue` in Bash viene utilizzato all'interno di cicli per saltare l'iterazione corrente e passare direttamente alla successiva. È particolarmente utile quando si desidera ignorare determinate condizioni senza interrompere l'intero ciclo.

## Usage
La sintassi di base del comando è la seguente:

```bash
continue [n]
```

Dove `n` è un numero opzionale che indica quante iterazioni del ciclo devono essere saltate. Se non specificato, il valore predefinito è 1.

## Common Options
- `n`: Numero di iterazioni da saltare. Se omesso, il comando salta solo l'iterazione corrente.

## Common Examples

### Esempio 1: Ignorare numeri dispari
Questo esempio mostra come utilizzare `continue` per ignorare i numeri dispari in un ciclo `for`.

```bash
for i in {1..10}; do
    if (( i % 2 != 0 )); then
        continue
    fi
    echo "Numero pari: $i"
done
```

### Esempio 2: Saltare file non leggibili
In questo esempio, si utilizza `continue` per saltare file che non possono essere letti in una directory.

```bash
for file in *; do
    if [ ! -r "$file" ]; then
        continue
    fi
    echo "File leggibile: $file"
done
```

### Esempio 3: Saltare iterazioni in un ciclo while
Utilizzando `continue` in un ciclo `while` per saltare le iterazioni basate su una condizione.

```bash
count=1
while [ $count -le 10 ]; do
    (( count % 3 == 0 )) && { count=$((count + 1)); continue; }
    echo "Numero: $count"
    ((count++))
done
```

## Tips
- Utilizza `continue` per migliorare la leggibilità del codice, evitando annidamenti complessi di `if`.
- Ricorda che `continue` influisce solo sul ciclo in cui è chiamato; non interrompe l'esecuzione di script o di altri cicli.
- Sii cauto nell'uso di `continue` in cicli annidati, poiché salterà solo l'iterazione del ciclo più interno.