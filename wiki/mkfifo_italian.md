# [Linux] Bash mkfifo utilizzo: Crea file FIFO (named pipes)

## Overview
Il comando `mkfifo` viene utilizzato per creare file FIFO, noti anche come named pipes. Questi file consentono la comunicazione tra processi in modo che un processo possa scrivere dati in un file e un altro processo possa leggerli.

## Usage
La sintassi di base del comando è la seguente:

```bash
mkfifo [opzioni] [file]
```

## Common Options
- `-m, --mode=MODE`: Imposta i permessi del file FIFO creato, dove `MODE` è in formato ottale.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `--version`: Mostra la versione del comando `mkfifo`.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `mkfifo`:

### Creare un file FIFO di base
```bash
mkfifo mio_fifo
```

### Creare un file FIFO con permessi specifici
```bash
mkfifo -m 644 mio_fifo
```

### Utilizzare un file FIFO in un esempio di comunicazione tra processi
1. In un terminale, avvia un comando per leggere dal FIFO:
   ```bash
   cat mio_fifo
   ```
2. In un altro terminale, scrivi nel FIFO:
   ```bash
   echo "Ciao, mondo!" > mio_fifo
   ```

### Creare più file FIFO contemporaneamente
```bash
mkfifo fifo1 fifo2 fifo3
```

## Tips
- Assicurati di avere i permessi corretti per scrivere e leggere dal file FIFO.
- Ricorda che i file FIFO bloccano la scrittura finché non c'è un processo in lettura, quindi è importante gestire correttamente i processi.
- Utilizza i file FIFO per facilitare la comunicazione tra script o applicazioni diverse in esecuzione contemporaneamente.