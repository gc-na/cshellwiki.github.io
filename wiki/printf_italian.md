# [Linux] Bash printf utilizzo: Formattare e stampare testo

## Overview
Il comando `printf` in Bash è utilizzato per formattare e stampare testo in modo controllato. A differenza di `echo`, `printf` offre maggiore flessibilità nel formattare l'output, permettendo di specificare il layout e il tipo di dati da visualizzare.

## Usage
La sintassi di base del comando `printf` è la seguente:

```bash
printf [opzioni] [argomenti]
```

## Common Options
- `-v`: Assegna l'output a una variabile invece di stamparlo.
- `-f`: Specifica un formato di output.
- `%s`: Formato per stringhe.
- `%d`: Formato per numeri interi.
- `%f`: Formato per numeri in virgola mobile.

## Common Examples
Ecco alcuni esempi pratici dell'uso di `printf`:

### Esempio 1: Stampa di una stringa
```bash
printf "Ciao, Mondo!\n"
```

### Esempio 2: Formattazione di numeri
```bash
printf "Il numero è: %d\n" 42
```

### Esempio 3: Stampa di più variabili
```bash
nome="Mario"
eta=30
printf "Nome: %s, Età: %d\n" "$nome" "$eta"
```

### Esempio 4: Formattazione di numeri in virgola mobile
```bash
printf "Il prezzo è: %.2f€\n" 19.99
```

### Esempio 5: Assegnazione a una variabile
```bash
printf -v messaggio "Benvenuto, %s!" "Giovanni"
echo "$messaggio"
```

## Tips
- Utilizza `\n` per andare a capo nel testo stampato.
- Ricorda di utilizzare le virgolette per le variabili per evitare problemi con spazi o caratteri speciali.
- Sperimenta con diversi formati per ottenere l'output desiderato, specialmente quando lavori con numeri.