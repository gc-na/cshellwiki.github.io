# [Linux] C Shell (csh) while: Esegue un ciclo condizionale

## Overview
Il comando `while` in C Shell (csh) è utilizzato per eseguire un blocco di comandi ripetutamente finché una condizione specificata rimane vera. È utile per automatizzare compiti ripetitivi e per gestire situazioni in cui è necessario continuare a eseguire un'operazione fino a quando non si verifica una certa condizione.

## Usage
La sintassi di base del comando `while` è la seguente:

```csh
while (condizione)
    comandi
end
```

## Common Options
Il comando `while` non ha opzioni specifiche, ma la condizione deve essere un'espressione valida che restituisce un valore booleano (vero o falso). 

## Common Examples

### Esempio 1: Contare fino a 5
```csh
set i = 1
while ($i <= 5)
    echo "Numero: $i"
    @ i++
end
```
Questo esempio conta da 1 a 5 e stampa ogni numero.

### Esempio 2: Leggere input fino a una condizione
```csh
set input = ""
while ("$input" != "exit")
    echo "Inserisci un comando (digita 'exit' per uscire):"
    set input = $< 
end
```
In questo caso, il ciclo continua a chiedere all'utente di inserire un comando fino a quando non viene digitata la parola "exit".

### Esempio 3: Eseguire un comando finché una condizione è vera
```csh
set count = 1
while ($count <= 10)
    echo "Esecuzione numero: $count"
    @ count++
end
```
Questo esempio esegue un'azione dieci volte, incrementando il contatore ad ogni iterazione.

## Tips
- Assicurati che la condizione del ciclo `while` possa diventare falsa; altrimenti, il ciclo continuerà indefinitamente.
- Utilizza la variabile `$?` per controllare il successo dell'ultimo comando eseguito all'interno del ciclo.
- Ricorda di utilizzare `@` per le operazioni aritmetiche, come l'incremento delle variabili.