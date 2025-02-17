# [Linux] Bash endif equivalente: Condizioni di fine

## Overview
Il comando `endif` in Bash è utilizzato per terminare una struttura condizionale iniziata con `if`. Non è un comando autonomo, ma piuttosto una parte della sintassi di controllo del flusso in uno script Bash. Serve a indicare la fine di un blocco condizionale.

## Usage
La sintassi di base del comando `endif` non viene scritta esplicitamente, poiché è implicita nella chiusura di un blocco `if`. Tuttavia, la struttura generale è la seguente:

```bash
if [ condizione ]; then
    # comandi da eseguire se la condizione è vera
fi
```

## Common Options
Poiché `endif` non è un comando autonomo, non ha opzioni specifiche. Le opzioni si riferiscono piuttosto al comando `if` e ai comandi all'interno del blocco condizionale.

## Common Examples

### Esempio 1: Condizione semplice
```bash
if [ -f "file.txt" ]; then
    echo "Il file esiste."
fi
```

### Esempio 2: Condizione con `else`
```bash
if [ -d "cartella" ]; then
    echo "La cartella esiste."
else
    echo "La cartella non esiste."
fi
```

### Esempio 3: Condizione con `elif`
```bash
if [ "$numero" -gt 10 ]; then
    echo "Il numero è maggiore di 10."
elif [ "$numero" -eq 10 ]; then
    echo "Il numero è uguale a 10."
else
    echo "Il numero è minore di 10."
fi
```

## Tips
- Assicurati di chiudere sempre il blocco `if` con `fi` per evitare errori di sintassi.
- Usa l'indentazione per migliorare la leggibilità del tuo codice, specialmente in script complessi.
- Ricorda che le condizioni possono essere combinate utilizzando operatori logici come `&&` e `||` per una maggiore flessibilità.