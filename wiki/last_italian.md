# [Linux] C Shell (csh) last comando: visualizza le ultime sessioni di accesso

## Overview
Il comando `last` in C Shell (csh) viene utilizzato per visualizzare un elenco delle ultime sessioni di accesso degli utenti al sistema. Mostra informazioni come il nome dell'utente, il terminale utilizzato, l'indirizzo IP e la data e l'ora di accesso.

## Usage
La sintassi di base del comando `last` è la seguente:

```
last [options] [arguments]
```

## Common Options
- `-n [numero]`: Specifica il numero di accessi da visualizzare.
- `-R`: Non mostra i nomi degli host, visualizzando solo gli accessi locali.
- `-f [file]`: Specifica un file di registro alternativo da cui leggere le informazioni di accesso.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `last`:

1. Visualizzare le ultime sessioni di accesso:
   ```csh
   last
   ```

2. Visualizzare solo le ultime 5 sessioni di accesso:
   ```csh
   last -n 5
   ```

3. Visualizzare le sessioni di accesso senza i nomi degli host:
   ```csh
   last -R
   ```

4. Leggere da un file di registro specifico:
   ```csh
   last -f /var/log/wtmp.1
   ```

## Tips
- Utilizza l'opzione `-n` per limitare l'output e rendere più facile la lettura delle informazioni.
- Controlla regolarmente le sessioni di accesso per monitorare attività sospette nel sistema.
- Puoi combinare `last` con altri comandi come `grep` per filtrare i risultati in base a un utente specifico. Ad esempio:
   ```csh
   last | grep nome_utente
   ```