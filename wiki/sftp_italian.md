# [Linux] C Shell (csh) sftp utilizzo: trasferimento sicuro di file

## Overview
Il comando `sftp` (SSH File Transfer Protocol) è utilizzato per trasferire file in modo sicuro tra un client e un server tramite una connessione SSH. È una versione più sicura del protocollo FTP e consente di caricare e scaricare file in modo semplice e protetto.

## Usage
La sintassi di base del comando `sftp` è la seguente:

```csh
sftp [opzioni] [utente@host]
```

## Common Options
Ecco alcune opzioni comuni per il comando `sftp`:

- `-P <port>`: Specifica una porta diversa da quella predefinita (22) per la connessione.
- `-o <option>`: Permette di specificare opzioni di configurazione SSH, come `UserKnownHostsFile` o `StrictHostKeyChecking`.
- `-b <file>`: Utilizza un file di batch per eseguire comandi `sftp` in modo non interattivo.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `sftp`:

1. **Connessione a un server SFTP**:
   ```csh
   sftp user@hostname
   ```

2. **Trasferire un file dal client al server**:
   ```csh
   put localfile.txt
   ```

3. **Scaricare un file dal server al client**:
   ```csh
   get remotefile.txt
   ```

4. **Visualizzare i file nella directory remota**:
   ```csh
   ls
   ```

5. **Creare una directory remota**:
   ```csh
   mkdir newdirectory
   ```

## Tips
- Assicurati di avere le credenziali corrette per connetterti al server SFTP.
- Utilizza l'opzione `-P` se il server SFTP utilizza una porta diversa dalla predefinita.
- Per trasferimenti di file di grandi dimensioni, considera l'uso di `-b` per automatizzare il processo con uno script di batch.