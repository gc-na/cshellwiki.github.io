# [Linux] Bash uname utilizzo: Ottieni informazioni sul sistema

## Overview
Il comando `uname` è utilizzato per ottenere informazioni sul sistema operativo in uso. Fornisce dettagli come il nome del kernel, la versione, l'architettura e altre informazioni utili per la gestione del sistema.

## Usage
La sintassi di base del comando è la seguente:

```bash
uname [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `uname`:

- `-a`: Mostra tutte le informazioni disponibili sul sistema.
- `-s`: Mostra il nome del kernel.
- `-n`: Mostra il nome del nodo di rete.
- `-r`: Mostra la versione del kernel.
- `-v`: Mostra la data di rilascio del kernel.
- `-m`: Mostra l'architettura della macchina.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `uname`:

1. **Mostrare tutte le informazioni sul sistema:**

   ```bash
   uname -a
   ```

2. **Mostrare solo il nome del kernel:**

   ```bash
   uname -s
   ```

3. **Mostrare la versione del kernel:**

   ```bash
   uname -r
   ```

4. **Mostrare l'architettura della macchina:**

   ```bash
   uname -m
   ```

5. **Mostrare il nome del nodo di rete:**

   ```bash
   uname -n
   ```

## Tips
- Utilizza `uname -a` per ottenere una panoramica completa del sistema in un solo comando.
- Puoi combinare le opzioni per ottenere informazioni specifiche; ad esempio, `uname -sr` mostra sia il nome del kernel che la sua versione.
- Ricorda che l'output di `uname` può variare a seconda del sistema operativo e della sua configurazione.