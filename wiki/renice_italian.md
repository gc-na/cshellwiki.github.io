# [Linux] Bash renice uso: Modifica la priorità dei processi in esecuzione

## Overview
Il comando `renice` in Bash viene utilizzato per modificare la priorità di esecuzione dei processi già in esecuzione. La priorità determina quanto tempo della CPU un processo può utilizzare rispetto ad altri processi. Un valore di priorità più basso significa una maggiore priorità.

## Usage
La sintassi di base del comando `renice` è la seguente:

```bash
renice [opzioni] [valore] [PID...]
```

## Common Options
- `-n`, `--priority`: Specifica il nuovo valore di priorità. Può essere un numero intero da -20 (massima priorità) a 19 (minima priorità).
- `-p`, `--pid`: Indica che il valore di priorità deve essere applicato ai processi specificati dai loro ID di processo (PID).
- `-g`, `--pgrp`: Modifica la priorità di tutti i processi in un gruppo di processi specificato.
- `-u`, `--user`: Modifica la priorità di tutti i processi appartenenti a un utente specificato.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `renice`:

1. **Modificare la priorità di un singolo processo**:
   Per aumentare la priorità di un processo con PID 1234 a -5:
   ```bash
   renice -n -5 -p 1234
   ```

2. **Modificare la priorità di più processi**:
   Per impostare la priorità a 10 per i processi con PID 1234 e 5678:
   ```bash
   renice -n 10 -p 1234 5678
   ```

3. **Modificare la priorità di tutti i processi di un utente**:
   Per abbassare la priorità di tutti i processi dell'utente "mario" a 15:
   ```bash
   renice -n 15 -u mario
   ```

4. **Modificare la priorità di un gruppo di processi**:
   Per aumentare la priorità di tutti i processi nel gruppo di processi con ID 1000 a -3:
   ```bash
   renice -n -3 -g 1000
   ```

## Tips
- Assicurati di avere i permessi necessari per modificare la priorità dei processi, in quanto potrebbe essere necessario eseguire il comando come superutente (utilizzando `sudo`).
- Usa valori di priorità con cautela; abbassare eccessivamente la priorità di un processo critico potrebbe influire sulle prestazioni del sistema.
- Controlla la priorità attuale dei processi utilizzando il comando `ps` o `top` prima di applicare `renice`.