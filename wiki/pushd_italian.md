# [Linux] Bash pushd uso: Cambiare directory in modo efficiente

## Overview
Il comando `pushd` in Bash è utilizzato per cambiare la directory corrente e memorizzare la directory precedente nella stack. Questo permette di navigare facilmente tra le directory senza perdere il percorso originale.

## Usage
La sintassi di base del comando è la seguente:

```bash
pushd [opzioni] [argomenti]
```

## Common Options
- `+n`: Ritorna alla directory n-esima nella stack.
- `-n`: Ritorna alla directory precedente senza aggiungere una nuova directory alla stack.
- `-q`: Esegue il comando in modalità silenziosa, non mostrando la directory corrente.

## Common Examples
Ecco alcuni esempi pratici dell'uso di `pushd`:

### Esempio 1: Cambiare directory
```bash
pushd /path/to/directory
```
Questo comando cambia la directory corrente a `/path/to/directory` e memorizza la directory precedente.

### Esempio 2: Tornare alla directory precedente
```bash
pushd -
```
Questo comando torna alla directory precedente che è stata memorizzata nella stack.

### Esempio 3: Navigare tra più directory
```bash
pushd /path/to/first-directory
pushd /path/to/second-directory
```
Qui, il primo comando cambia a `first-directory`, e il secondo comando cambia a `second-directory`, memorizzando `first-directory` nella stack.

### Esempio 4: Usare l'opzione +n
```bash
pushd +0
```
Questo comando ritorna alla directory attualmente in cima alla stack.

## Tips
- Utilizza `dirs` per visualizzare la stack delle directory memorizzate.
- Ricorda che `pushd` può essere combinato con `popd` per tornare indietro nella navigazione.
- Usa `pushd` in script per gestire facilmente le directory senza perdere il contesto.