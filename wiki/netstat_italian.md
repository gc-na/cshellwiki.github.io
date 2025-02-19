# [Linux] C Shell (csh) netstat Utilizzo: Visualizzare le connessioni di rete

## Overview
Il comando `netstat` è uno strumento utile per visualizzare le connessioni di rete attive, le tabelle di routing e le statistiche delle interfacce di rete. È particolarmente utile per il monitoraggio delle attività di rete e la risoluzione dei problemi.

## Usage
La sintassi di base del comando `netstat` è la seguente:

```
netstat [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `netstat`:

- `-a`: Mostra tutte le connessioni e le porte in ascolto.
- `-t`: Visualizza solo le connessioni TCP.
- `-u`: Visualizza solo le connessioni UDP.
- `-n`: Mostra gli indirizzi e i numeri di porta in formato numerico.
- `-r`: Mostra la tabella di routing.
- `-i`: Mostra le statistiche delle interfacce di rete.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `netstat`:

1. **Visualizzare tutte le connessioni attive:**
   ```bash
   netstat -a
   ```

2. **Visualizzare solo le connessioni TCP:**
   ```bash
   netstat -t
   ```

3. **Visualizzare le statistiche delle interfacce di rete:**
   ```bash
   netstat -i
   ```

4. **Visualizzare la tabella di routing:**
   ```bash
   netstat -r
   ```

5. **Visualizzare le connessioni in formato numerico:**
   ```bash
   netstat -n
   ```

## Tips
- Utilizza l'opzione `-p` per visualizzare il processo associato a ciascuna connessione, se supportato.
- Combina più opzioni per ottenere informazioni più dettagliate, ad esempio `netstat -tuln` per vedere le connessioni TCP e UDP in ascolto in formato numerico.
- Ricorda che l'esecuzione di `netstat` potrebbe richiedere privilegi di amministratore per visualizzare tutte le informazioni.