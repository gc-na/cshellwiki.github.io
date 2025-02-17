# [Linux] Bash command uso: [eseguire comandi in background]

## Overview
Il comando `nohup` viene utilizzato per eseguire un comando in background, permettendo di continuare l'esecuzione anche dopo che l'utente ha disconnesso la sessione. Questo è particolarmente utile per processi lunghi che non devono essere interrotti.

## Usage
La sintassi di base del comando `nohup` è la seguente:

```bash
nohup command [options] [arguments] &
```

## Common Options
- `&`: Esegue il comando in background.
- `-h`: Mostra un messaggio di aiuto con le opzioni disponibili (non sempre presente).
- `output_file`: Puoi reindirizzare l'output standard e l'output di errore in un file specificato.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `nohup`:

1. Eseguire uno script in background:
   ```bash
   nohup ./myscript.sh &
   ```

2. Eseguire un comando lungo e reindirizzare l'output in un file:
   ```bash
   nohup long_running_command > output.log 2>&1 &
   ```

3. Eseguire un comando di aggiornamento del sistema in background:
   ```bash
   nohup sudo apt update && sudo apt upgrade -y &
   ```

4. Eseguire un server web in background:
   ```bash
   nohup python3 -m http.server 8000 &
   ```

## Tips
- Assicurati di usare `&` alla fine del comando per eseguirlo in background.
- Controlla il file `nohup.out` per l'output se non hai specificato un file di output.
- Usa il comando `jobs` per visualizzare i processi in background attivi nella tua sessione.