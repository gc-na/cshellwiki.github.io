# [Linux] Bash killall Uso: Termina i processi in base al nome

## Overview
Il comando `killall` viene utilizzato per terminare i processi in esecuzione sul sistema operativo Linux, specificando il nome del processo. È utile per gestire i processi che non rispondono o per liberare risorse di sistema.

## Usage
La sintassi di base del comando `killall` è la seguente:

```bash
killall [opzioni] [nome_del_processo]
```

## Common Options
- `-i`: Chiede conferma prima di terminare ogni processo.
- `-q`: Non mostra messaggi di errore se il processo non esiste.
- `-r`: Usa espressioni regolari per il nome del processo.
- `-s`: Specifica il segnale da inviare al processo (ad esempio, `-s SIGKILL`).

## Common Examples
Ecco alcuni esempi pratici dell'uso di `killall`:

1. Terminare un processo specifico per nome:
   ```bash
   killall firefox
   ```

2. Terminare tutti i processi di un'applicazione con conferma:
   ```bash
   killall -i gedit
   ```

3. Usare un'espressione regolare per terminare processi:
   ```bash
   killall -r 'python.*'
   ```

4. Inviare un segnale specifico per terminare un processo:
   ```bash
   killall -s SIGKILL chrome
   ```

## Tips
- Assicurati di avere i permessi necessari per terminare i processi; potresti dover usare `sudo` per processi di sistema.
- Usa l'opzione `-i` per evitare di terminare accidentalmente processi importanti.
- Controlla i processi attivi con `ps aux` prima di utilizzare `killall` per evitare di chiudere processi critici.