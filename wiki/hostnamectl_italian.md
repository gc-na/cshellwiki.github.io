# [Linux] Bash hostnamectl utilizzo: Gestire il nome host di un sistema

## Overview
Il comando `hostnamectl` è utilizzato per visualizzare e modificare il nome host di un sistema Linux. Permette di gestire il nome statico, il nome transitorio e il nome locale del computer, facilitando la configurazione della rete e l'identificazione del sistema.

## Usage
La sintassi di base del comando è la seguente:

```bash
hostnamectl [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `hostnamectl`:

- `set-hostname`: Imposta il nome host statico del sistema.
- `set-icon-name`: Imposta un nome icona per il sistema.
- `set-chassis`: Imposta il tipo di chassis del sistema (es. desktop, server).
- `status`: Mostra lo stato attuale del nome host e altre informazioni correlate.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `hostnamectl`:

1. **Visualizzare le informazioni attuali del sistema:**
   ```bash
   hostnamectl status
   ```

2. **Impostare un nuovo nome host statico:**
   ```bash
   sudo hostnamectl set-hostname nuovo-nome-host
   ```

3. **Impostare un nome icona:**
   ```bash
   sudo hostnamectl set-icon-name icona-nome
   ```

4. **Impostare il tipo di chassis:**
   ```bash
   sudo hostnamectl set-chassis server
   ```

## Tips
- Assicurati di avere i privilegi di amministratore (sudo) quando imposti un nuovo nome host.
- Dopo aver cambiato il nome host, potrebbe essere necessario riavviare il sistema o riavviare i servizi di rete per applicare le modifiche.
- Usa `hostnamectl status` per verificare che il nuovo nome host sia stato impostato correttamente.