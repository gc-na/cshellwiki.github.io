# [Linux] Bash dstat utilizzo: Monitora le risorse di sistema in tempo reale

## Overview
Il comando `dstat` è uno strumento versatile per il monitoraggio delle risorse di sistema in tempo reale. Combina le funzionalità di vari strumenti di monitoraggio, fornendo informazioni su CPU, memoria, disco, rete e altro in un formato facilmente leggibile.

## Usage
La sintassi di base del comando `dstat` è la seguente:

```bash
dstat [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `dstat`:

- `-c`: Mostra l'utilizzo della CPU.
- `-d`: Mostra l'attività del disco.
- `-n`: Mostra l'attività di rete.
- `-m`: Mostra l'utilizzo della memoria.
- `--time`: Mostra il timestamp per ogni riga di output.
- `-r`: Mostra l'utilizzo della memoria di swap.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `dstat`:

1. **Monitorare l'utilizzo della CPU e della memoria:**

   ```bash
   dstat -c -m
   ```

2. **Visualizzare l'attività del disco e della rete:**

   ```bash
   dstat -d -n
   ```

3. **Monitorare tutte le risorse con timestamp:**

   ```bash
   dstat --time -cdmn
   ```

4. **Monitorare l'utilizzo della memoria di swap:**

   ```bash
   dstat -r
   ```

## Tips
- Utilizza `dstat` con l'opzione `-t` per avere un timestamp, utile per registrare eventi nel tempo.
- Puoi combinare diverse opzioni per ottenere un output più dettagliato e personalizzato.
- Considera di eseguire `dstat` in background e reindirizzare l'output a un file per analisi successive.

Con `dstat`, puoi ottenere una visione chiara e immediata delle prestazioni del tuo sistema, rendendolo uno strumento indispensabile per amministratori di sistema e sviluppatori.