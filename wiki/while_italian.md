# [Linux] Bash while utilizzo: Esegue un blocco di comandi ripetutamente

## Overview
Il comando `while` in Bash è utilizzato per eseguire un blocco di comandi ripetutamente finché una condizione specificata è vera. È particolarmente utile per iterare su un insieme di dati o per eseguire operazioni fino a quando non si verifica una certa condizione.

## Usage
La sintassi di base del comando `while` è la seguente:

```bash
while [condizione]
do
    # comandi da eseguire
done
```

## Common Options
Il comando `while` non ha opzioni specifiche, ma la condizione può essere espressa in vari modi, come ad esempio:

- `[ -n stringa ]`: vero se la stringa non è vuota.
- `[ -z stringa ]`: vero se la stringa è vuota.
- `[ numero -eq numero ]`: vero se i numeri sono uguali.
- `[ numero -lt numero ]`: vero se il primo numero è minore del secondo.

## Common Examples

### Esempio 1: Contare fino a 5
```bash
count=1
while [ $count -le 5 ]
do
    echo "Conto: $count"
    ((count++))
done
```

### Esempio 2: Leggere file riga per riga
```bash
while IFS= read -r line
do
    echo "Riga: $line"
done < file.txt
```

### Esempio 3: Eseguire un comando finché non si ottiene un risultato
```bash
while ! ping -c 1 google.com
do
    echo "In attesa di connessione..."
    sleep 2
done
echo "Connessione stabilita!"
```

## Tips
- Assicurati che la condizione del ciclo `while` possa eventualmente diventare falsa, altrimenti il ciclo continuerà indefinitamente.
- Usa `sleep` all'interno del ciclo per evitare un utilizzo eccessivo della CPU in caso di cicli rapidi.
- Puoi utilizzare `break` per uscire dal ciclo `while` in base a una condizione interna, se necessario.