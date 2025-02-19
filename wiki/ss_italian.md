# [Linux] C Shell (csh) ss Utilizzo: Visualizza le connessioni di rete

## Overview
Il comando `ss` è utilizzato per visualizzare le connessioni di rete, le porte in ascolto e le statistiche delle socket. È uno strumento utile per il monitoraggio delle connessioni TCP e UDP sul sistema.

## Usage
La sintassi di base del comando è la seguente:

```bash
ss [opzioni] [argomenti]
```

## Common Options
- `-t`: Mostra solo le connessioni TCP.
- `-u`: Mostra solo le connessioni UDP.
- `-l`: Visualizza solo le porte in ascolto.
- `-p`: Mostra i processi che utilizzano le connessioni.
- `-n`: Disabilita la risoluzione dei nomi, mostrando gli indirizzi numerici.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `ss`:

1. Visualizzare tutte le connessioni TCP attive:
   ```bash
   ss -t
   ```

2. Visualizzare tutte le porte in ascolto:
   ```bash
   ss -l
   ```

3. Visualizzare le connessioni UDP:
   ```bash
   ss -u
   ```

4. Visualizzare le connessioni con i processi associati:
   ```bash
   ss -p
   ```

5. Visualizzare le connessioni senza risoluzione dei nomi:
   ```bash
   ss -n
   ```

## Tips
- Utilizza `ss -t -l` per vedere quali porte TCP sono in ascolto sul tuo sistema.
- Combina più opzioni per ottenere informazioni più dettagliate, ad esempio `ss -tunlp` per vedere tutte le connessioni TCP e UDP con i processi associati.
- Ricorda che l'esecuzione di `ss` potrebbe richiedere privilegi di amministratore per visualizzare tutte le connessioni.