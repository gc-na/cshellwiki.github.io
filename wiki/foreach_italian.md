# [Linux] C Shell (csh) foreach utilizzo: Esegue un comando per ogni elemento in una lista

## Overview
Il comando `foreach` nel C Shell (csh) consente di eseguire un insieme di comandi per ogni elemento di una lista. È utile per automatizzare operazioni ripetitive su più file o argomenti.

## Usage
La sintassi di base del comando `foreach` è la seguente:

```csh
foreach variabile (lista)
    comandi
end
```

## Common Options
Il comando `foreach` non ha molte opzioni, ma è importante sapere che:
- `variabile`: rappresenta il nome della variabile che assumerà il valore di ciascun elemento della lista ad ogni iterazione.
- `lista`: è un elenco di elementi su cui si desidera iterare.

## Common Examples

### Esempio 1: Iterare su una lista di nomi di file
```csh
foreach file (*.txt)
    echo "Elaborando il file: $file"
end
```
In questo esempio, il comando `echo` verrà eseguito per ogni file con estensione `.txt` nella directory corrente.

### Esempio 2: Eseguire un comando su più directory
```csh
foreach dir (dir1 dir2 dir3)
    cd $dir
    ls
    cd ..
end
```
Qui, il comando `ls` verrà eseguito in ciascuna delle directory specificate.

### Esempio 3: Applicare un comando a una lista di numeri
```csh
foreach numero (1 2 3 4 5)
    @ risultato = $numero * 2
    echo "Il doppio di $numero è $risultato"
end
```
Questo esempio calcola e stampa il doppio di ciascun numero nella lista.

## Tips
- Assicurati di utilizzare il comando `end` per terminare il blocco `foreach`.
- Puoi utilizzare wildcard per selezionare file in modo dinamico.
- Ricorda che le variabili all'interno del blocco `foreach` sono locali e non influenzano il resto dello script.