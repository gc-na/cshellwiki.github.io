# [Linux] C Shell (csh) groupmod uso: Modificare le informazioni di un gruppo

## Overview
Il comando `groupmod` viene utilizzato per modificare le informazioni di un gruppo esistente nel sistema. Consente di cambiare il nome del gruppo o il suo identificatore (GID), facilitando la gestione degli utenti e dei gruppi.

## Usage
La sintassi di base del comando è la seguente:

```
groupmod [opzioni] [argomenti]
```

## Common Options
- `-n, --new-name`: Cambia il nome del gruppo.
- `-g, --gid`: Cambia l'identificatore del gruppo (GID).
- `-o, --non-unique`: Permette di utilizzare un GID non univoco.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `groupmod`:

1. **Cambia il nome di un gruppo**:
   ```bash
   groupmod -n nuovo_nome_gruppo vecchio_nome_gruppo
   ```

2. **Cambia il GID di un gruppo**:
   ```bash
   groupmod -g 1001 nome_gruppo
   ```

3. **Cambia il nome e il GID di un gruppo**:
   ```bash
   groupmod -n nuovo_nome_gruppo -g 1002 vecchio_nome_gruppo
   ```

## Tips
- Assicurati di avere i privilegi di amministratore per eseguire il comando `groupmod`.
- Controlla sempre che il nuovo GID non sia già in uso da un altro gruppo per evitare conflitti.
- Dopo aver modificato un gruppo, verifica le modifiche utilizzando il comando `getent group nome_gruppo`.