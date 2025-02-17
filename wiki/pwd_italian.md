# [Linux] Bash pwd utilizzo: mostrare il percorso corrente

## Overview
Il comando `pwd` (print working directory) è utilizzato per visualizzare il percorso della directory corrente in cui ci si trova nel terminale. È uno strumento fondamentale per navigare nel filesystem di Linux e per comprendere la propria posizione all'interno della struttura delle cartelle.

## Usage
La sintassi di base del comando `pwd` è la seguente:

```bash
pwd [opzioni]
```

## Common Options
Ecco alcune opzioni comuni per il comando `pwd`:

- `-L`: Mostra il percorso logico, seguendo i collegamenti simbolici.
- `-P`: Mostra il percorso fisico, risolvendo i collegamenti simbolici e mostrando il percorso reale.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `pwd`:

1. **Visualizzare il percorso corrente:**
   ```bash
   pwd
   ```

2. **Visualizzare il percorso logico:**
   ```bash
   pwd -L
   ```

3. **Visualizzare il percorso fisico:**
   ```bash
   pwd -P
   ```

## Tips
- Utilizza `pwd` frequentemente per tenere traccia della tua posizione nel filesystem, specialmente quando lavori in directory profonde.
- Ricorda che `pwd` è utile anche quando si scrivono script, per assicurarsi di operare nella directory corretta.
- Se stai utilizzando collegamenti simbolici, considera l'uso dell'opzione `-P` per ottenere il percorso reale.