# [Linux] Bash groupmod uso: Modifica le proprietà di un gruppo

## Overview
Il comando `groupmod` in Bash viene utilizzato per modificare le proprietà di un gruppo esistente nel sistema. Questo comando consente di cambiare il nome del gruppo, il GID (Group ID) e altre caratteristiche associate al gruppo.

## Usage
La sintassi di base del comando `groupmod` è la seguente:

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name NEW_GROUP`: Cambia il nome del gruppo specificato con `NEW_GROUP`.
- `-g, --gid GID`: Modifica il GID del gruppo a quello specificato.
- `-o, --non-unique`: Permette di utilizzare un GID non univoco, utile se si desidera assegnare lo stesso GID a più gruppi.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `groupmod`:

1. **Modificare il nome di un gruppo**:
   ```bash
   groupmod -n nuovo_nome gruppo_esistente
   ```

2. **Cambiare il GID di un gruppo**:
   ```bash
   groupmod -g 1001 gruppo_esistente
   ```

3. **Modificare il nome e il GID di un gruppo**:
   ```bash
   groupmod -n nuovo_nome -g 1001 gruppo_esistente
   ```

4. **Consentire un GID non univoco**:
   ```bash
   groupmod -o -g 1001 gruppo_esistente
   ```

## Tips
- Assicurati di avere i privilegi di superutente (root) per eseguire il comando `groupmod`, poiché le modifiche ai gruppi richiedono autorizzazioni elevate.
- Controlla sempre i gruppi esistenti e i loro GID prima di apportare modifiche, per evitare conflitti.
- Dopo aver modificato un gruppo, verifica le modifiche utilizzando il comando `getent group` per assicurarti che tutto sia stato aggiornato correttamente.