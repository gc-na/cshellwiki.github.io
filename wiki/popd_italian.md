# [Linux] Bash popd utilizzo: Rimuove la directory superiore dalla stack

## Overview
Il comando `popd` in Bash è utilizzato per rimuovere la directory superiore dalla stack delle directory. Questo comando è utile quando si naviga tra diverse directory utilizzando `pushd`, permettendo di tornare rapidamente alla directory precedente.

## Usage
La sintassi di base del comando è la seguente:

```bash
popd [options] [arguments]
```

## Common Options
- `+n`: Rimuove la directory n-esima dalla stack, dove n è un numero intero.
- `-n`: Rimuove la directory n-esima dalla fine della stack, dove n è un numero intero.

## Common Examples

1. **Tornare alla directory precedente**:
   ```bash
   popd
   ```

2. **Rimuovere la seconda directory dalla stack**:
   ```bash
   popd +1
   ```

3. **Rimuovere l'ultima directory dalla stack**:
   ```bash
   popd -1
   ```

4. **Visualizzare la stack delle directory prima di usare popd**:
   ```bash
   dirs
   ```

## Tips
- Utilizza `pushd` per aggiungere directory alla stack prima di usare `popd`, in modo da gestire facilmente la navigazione tra più directory.
- Controlla frequentemente la tua stack delle directory con il comando `dirs` per tenere traccia delle directory attive.
- Ricorda che `popd` funziona solo se hai precedentemente utilizzato `pushd` per aggiungere directory alla stack.