# [Linux] Bash dirs uso: Visualizza la lista delle directory

## Overview
Il comando `dirs` in Bash è utilizzato per visualizzare la lista delle directory attualmente memorizzate nello stack delle directory. Questo stack è utile per navigare rapidamente tra le directory utilizzate di recente.

## Usage
La sintassi di base del comando è la seguente:

```bash
dirs [options] [arguments]
```

## Common Options
- `-l`: Mostra la lista delle directory in formato lungo, includendo il percorso completo.
- `-p`: Mostra le directory in un formato compatto, separando i percorsi con spazi.
- `+N`: Mostra la directory alla posizione N nello stack.
- `-N`: Mostra la directory alla posizione N contando dalla fine dello stack.

## Common Examples

1. **Visualizzare le directory correnti**:
   ```bash
   dirs
   ```

2. **Visualizzare le directory in formato lungo**:
   ```bash
   dirs -l
   ```

3. **Visualizzare la terza directory nello stack**:
   ```bash
   dirs +2
   ```

4. **Visualizzare la seconda directory contando dalla fine**:
   ```bash
   dirs -2
   ```

5. **Aggiungere una directory allo stack e visualizzarla**:
   ```bash
   cd /path/to/directory
   dirs
   ```

## Tips
- Utilizza `pushd` e `popd` insieme a `dirs` per gestire facilmente lo stack delle directory.
- Ricorda che `dirs` mostra solo le directory nello stack, quindi assicurati di utilizzare `pushd` per aggiungere directory.
- Puoi utilizzare `dirs -p` per una visualizzazione più compatta quando hai molte directory nello stack.