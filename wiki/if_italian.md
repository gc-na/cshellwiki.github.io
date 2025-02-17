# [Linux] Bash if: Esegui comandi condizionali

## Overview
Il comando `if` in Bash è utilizzato per eseguire comandi condizionali. Permette di eseguire un blocco di codice solo se una determinata condizione è vera. È uno strumento fondamentale per il controllo del flusso nei script Bash.

## Usage
La sintassi di base del comando `if` è la seguente:

```bash
if [ condizione ]; then
    # comandi da eseguire se la condizione è vera
fi
```

## Common Options
- `-e`: Verifica se un file esiste.
- `-d`: Controlla se un percorso è una directory.
- `-f`: Controlla se un percorso è un file regolare.
- `-z`: Verifica se una stringa è vuota.
- `-n`: Verifica se una stringa non è vuota.

## Common Examples

### Esempio 1: Verifica se un file esiste
```bash
if [ -e "file.txt" ]; then
    echo "Il file esiste."
else
    echo "Il file non esiste."
fi
```

### Esempio 2: Controlla se una variabile è vuota
```bash
variabile=""
if [ -z "$variabile" ]; then
    echo "La variabile è vuota."
else
    echo "La variabile non è vuota."
fi
```

### Esempio 3: Verifica se una directory esiste
```bash
if [ -d "/path/to/directory" ]; then
    echo "La directory esiste."
else
    echo "La directory non esiste."
fi
```

### Esempio 4: Confronto di numeri
```bash
numero=10
if [ $numero -gt 5 ]; then
    echo "Il numero è maggiore di 5."
fi
```

## Tips
- Ricorda di usare sempre gli spazi corretti all'interno delle parentesi quadre.
- Puoi concatenare più condizioni usando `&&` (e) o `||` (o) per creare logiche più complesse.
- Utilizza le parentesi graffe `{}` per delimitare variabili quando necessario, specialmente in contesti complessi.