# [Linux] Bash cd uso: Cambiare directory nel filesystem

## Overview
Il comando `cd` (change directory) è utilizzato per navigare tra le directory nel filesystem di un sistema operativo basato su Unix. Permette all'utente di spostarsi in diverse cartelle per gestire file e directory in modo più efficiente.

## Usage
La sintassi di base del comando `cd` è la seguente:

```bash
cd [opzioni] [argomenti]
```

## Common Options
- `..` : Ritorna alla directory padre.
- `-` : Torna all'ultima directory visitata.
- `~` : Rappresenta la home directory dell'utente corrente.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `cd`:

1. **Navigare alla directory home**:
   ```bash
   cd ~
   ```

2. **Spostarsi in una directory specifica**:
   ```bash
   cd /percorso/della/directory
   ```

3. **Tornare alla directory precedente**:
   ```bash
   cd -
   ```

4. **Tornare alla directory padre**:
   ```bash
   cd ..
   ```

5. **Navigare in una sottodirectory**:
   ```bash
   cd cartella_sottodirectory
   ```

## Tips
- Utilizza `cd -` per tornare rapidamente all'ultima directory visitata, risparmiando tempo.
- Ricorda che puoi utilizzare il tab per completare automaticamente i nomi delle directory, rendendo la navigazione più veloce.
- Se hai bisogno di vedere dove ti trovi attualmente, puoi usare il comando `pwd` dopo `cd` per visualizzare il percorso completo della directory corrente.