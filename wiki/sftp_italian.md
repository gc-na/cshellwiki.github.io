# [Linux] Bash sftp utilizzo: trasferire file in modo sicuro

## Overview
Il comando `sftp` (SSH File Transfer Protocol) è uno strumento utilizzato per trasferire file in modo sicuro tra un client e un server. Utilizza il protocollo SSH per garantire che i dati siano criptati durante il trasferimento.

## Usage
La sintassi di base del comando `sftp` è la seguente:

```bash
sftp [opzioni] [utente@host]
```

## Common Options
Ecco alcune opzioni comuni per il comando `sftp`:

- `-i <file>`: Specifica un file di chiave privata per l'autenticazione.
- `-P <port>`: Specifica una porta diversa dalla porta predefinita (22) per la connessione.
- `-v`: Abilita la modalità verbosa, utile per il debug.
- `-b <file>`: Esegue comandi SFTP da un file batch.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `sftp`:

1. **Connessione a un server SFTP:**
   ```bash
   sftp user@hostname
   ```

2. **Trasferire un file dal client al server:**
   ```bash
   put /percorso/del/file locale.txt
   ```

3. **Scaricare un file dal server al client:**
   ```bash
   get remote.txt /percorso/dove/salvare/
   ```

4. **Visualizzare i file nella directory remota:**
   ```bash
   ls
   ```

5. **Creare una directory remota:**
   ```bash
   mkdir nuova_directory
   ```

## Tips
- Assicurati di avere i permessi necessari per accedere e modificare i file sul server.
- Utilizza la modalità verbosa (`-v`) per ottenere informazioni dettagliate durante la connessione e il trasferimento.
- Considera l'uso di chiavi SSH per una connessione più sicura e senza password.