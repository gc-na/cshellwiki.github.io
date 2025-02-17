# [Linux] Bash nohup utilizzo: Esegui comandi senza interruzioni

## Overview
Il comando `nohup` (no hang up) è utilizzato in Bash per eseguire processi in modo che continuino a funzionare anche dopo che l'utente ha disconnesso la sessione. Questo è particolarmente utile per eseguire script o comandi a lungo termine su server remoti.

## Usage
La sintassi di base del comando `nohup` è la seguente:

```bash
nohup [opzioni] [argomenti] &
```

L'ampersand (`&`) alla fine del comando serve a eseguire il processo in background.

## Common Options
- `-h`, `--help`: Mostra un messaggio di aiuto e termina.
- `-V`, `--version`: Mostra la versione del comando `nohup`.
- `-o FILE`: Specifica un file in cui scrivere l'output standard (default è `nohup.out`).
- `-e FILE`: Specifica un file in cui scrivere l'output di errore (default è `nohup.out`).

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `nohup`:

1. Eseguire uno script in background:
   ```bash
   nohup ./script.sh &
   ```

2. Eseguire un comando e reindirizzare l'output in un file specifico:
   ```bash
   nohup long_running_command > output.log &
   ```

3. Eseguire un comando e reindirizzare sia l'output che l'errore:
   ```bash
   nohup long_running_command > output.log 2>&1 &
   ```

4. Eseguire un processo in background e ignorare l'output:
   ```bash
   nohup some_command > /dev/null 2>&1 &
   ```

## Tips
- Assicurati di utilizzare l'ampersand (`&`) per eseguire il comando in background, altrimenti il terminale rimarrà bloccato fino al completamento del processo.
- Controlla il file `nohup.out` per eventuali messaggi di output o errori se non hai specificato un file di output personalizzato.
- Utilizza `jobs` per visualizzare i processi in background e `fg` per riportarli in primo piano se necessario.