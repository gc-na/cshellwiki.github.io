# [Linux] Bash netstat utilizzo: Visualizzare le connessioni di rete

## Overview
Il comando `netstat` è uno strumento utile per visualizzare le connessioni di rete attive, le tabelle di routing e le statistiche delle interfacce di rete. È particolarmente utile per diagnosticare problemi di rete e monitorare le attività di rete sul sistema.

## Usage
La sintassi di base del comando `netstat` è la seguente:

```bash
netstat [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `netstat`:

- `-a`: Mostra tutte le connessioni e le porte in ascolto.
- `-t`: Visualizza solo le connessioni TCP.
- `-u`: Visualizza solo le connessioni UDP.
- `-n`: Mostra gli indirizzi e i numeri di porta in formato numerico, evitando la risoluzione dei nomi.
- `-l`: Mostra solo le porte in ascolto.
- `-p`: Mostra il PID e il nome del programma associato a ciascuna connessione.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `netstat`:

1. **Visualizzare tutte le connessioni attive:**

   ```bash
   netstat -a
   ```

2. **Visualizzare solo le connessioni TCP:**

   ```bash
   netstat -t
   ```

3. **Visualizzare le porte in ascolto:**

   ```bash
   netstat -l
   ```

4. **Visualizzare le connessioni UDP:**

   ```bash
   netstat -u
   ```

5. **Visualizzare le connessioni con PID e nome del programma:**

   ```bash
   netstat -p
   ```

6. **Visualizzare le connessioni in formato numerico:**

   ```bash
   netstat -n
   ```

## Tips
- Utilizza l'opzione `-p` per identificare quali processi stanno utilizzando le connessioni di rete, utile per la risoluzione dei problemi.
- Combina le opzioni per ottenere informazioni più dettagliate, ad esempio `netstat -tuln` per vedere le connessioni TCP e UDP in ascolto in formato numerico.
- Ricorda che potrebbe essere necessario eseguire `netstat` con privilegi elevati (ad esempio, utilizzando `sudo`) per visualizzare tutte le connessioni e i processi.