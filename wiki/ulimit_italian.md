# [Linux] Bash ulimit utilizzo: Limita le risorse per i processi

## Overview
Il comando `ulimit` in Bash è utilizzato per controllare le risorse disponibili per i processi in esecuzione. Permette di impostare limiti su vari aspetti, come la quantità di memoria, il numero di file aperti e il tempo di CPU, per evitare che un singolo processo consumi tutte le risorse di sistema.

## Usage
La sintassi di base del comando `ulimit` è la seguente:

```bash
ulimit [options] [arguments]
```

## Common Options
- `-a`: Mostra tutti i limiti attuali.
- `-c`: Imposta la dimensione massima del core dump.
- `-d`: Imposta la dimensione massima della memoria dati.
- `-f`: Imposta la dimensione massima dei file creati.
- `-l`: Imposta la dimensione massima della memoria bloccata.
- `-n`: Imposta il numero massimo di file aperti.
- `-t`: Imposta il tempo massimo di CPU in secondi.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `ulimit`:

### Mostrare tutti i limiti
```bash
ulimit -a
```

### Impostare il numero massimo di file aperti a 1024
```bash
ulimit -n 1024
```

### Impostare la dimensione massima del core dump a 0 (disabilitare i core dump)
```bash
ulimit -c 0
```

### Impostare la dimensione massima dei file creati a 10 MB
```bash
ulimit -f 10240
```

### Impostare il tempo massimo di CPU a 60 secondi
```bash
ulimit -t 60
```

## Tips
- Utilizza `ulimit -a` per avere una panoramica dei limiti attuali prima di modificarli.
- Ricorda che i limiti impostati con `ulimit` sono validi solo per la sessione corrente della shell.
- Per rendere permanenti le modifiche, puoi aggiungere i comandi `ulimit` al tuo file di configurazione della shell, come `.bashrc` o `.bash_profile`.