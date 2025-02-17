# [Linux] Bash test uso: Verifica condizioni

## Overview
Il comando `test` in Bash è utilizzato per valutare espressioni condizionali. È comunemente usato in script per verificare file, confrontare stringhe e numeri, e determinare il flusso di esecuzione in base ai risultati delle valutazioni.

## Usage
La sintassi di base del comando `test` è la seguente:

```bash
test [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `test`:

- `-e FILE`: Verifica se il file esiste.
- `-f FILE`: Controlla se il file è un file regolare.
- `-d DIRECTORY`: Verifica se la directory esiste.
- `-z STRING`: Controlla se la lunghezza della stringa è zero.
- `-n STRING`: Controlla se la lunghezza della stringa è maggiore di zero.
- `NUM1 -eq NUM2`: Verifica se i due numeri sono uguali.
- `NUM1 -ne NUM2`: Verifica se i due numeri non sono uguali.
- `NUM1 -lt NUM2`: Verifica se NUM1 è minore di NUM2.
- `NUM1 -gt NUM2`: Verifica se NUM1 è maggiore di NUM2.

## Common Examples

Ecco alcuni esempi pratici dell'uso del comando `test`:

### Verifica se un file esiste
```bash
if test -e "file.txt"; then
    echo "Il file esiste."
else
    echo "Il file non esiste."
fi
```

### Controlla se una stringa è vuota
```bash
stringa=""
if test -z "$stringa"; then
    echo "La stringa è vuota."
else
    echo "La stringa non è vuota."
fi
```

### Confronto di numeri
```bash
num1=5
num2=10
if test $num1 -lt $num2; then
    echo "$num1 è minore di $num2."
fi
```

### Verifica se una directory esiste
```bash
if test -d "/path/to/directory"; then
    echo "La directory esiste."
else
    echo "La directory non esiste."
fi
```

## Tips
- Utilizza le parentesi quadre `[` e `]` come alternativa a `test`, ad esempio: `[ -e "file.txt" ]`.
- Ricorda di utilizzare spazi appropriati tra le opzioni e gli argomenti per evitare errori di sintassi.
- Puoi combinare più condizioni usando `&&` (AND) e `||` (OR) per creare espressioni più complesse.