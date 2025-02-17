# [Linux] Bash ftp utilizzo: Comando per trasferire file tramite il protocollo FTP

## Overview
Il comando `ftp` (File Transfer Protocol) è utilizzato per trasferire file tra un client e un server su una rete. Consente di caricare e scaricare file, gestire directory e eseguire altre operazioni relative ai file su un server FTP.

## Usage
La sintassi di base del comando `ftp` è la seguente:

```bash
ftp [opzioni] [argomenti]
```

## Common Options
- `-i`: Disabilita la modalità interattiva, utile per trasferimenti di file in batch.
- `-v`: Abilita la modalità verbosa, mostrando informazioni dettagliate durante il trasferimento.
- `-n`: Disabilita l'accesso automatico al server FTP all'avvio.
- `-p`: Usa una connessione passiva, utile per attraversare firewall.
- `-g`: Disabilita l'espansione dei caratteri jolly.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `ftp`:

### Connessione a un server FTP
```bash
ftp ftp.example.com
```

### Scaricare un file dal server
```bash
get nomefile.txt
```

### Caricare un file sul server
```bash
put nomefile.txt
```

### Elencare i file nella directory corrente del server
```bash
ls
```

### Cambiare directory sul server
```bash
cd /path/to/directory
```

### Uscire dalla sessione FTP
```bash
bye
```

## Tips
- Assicurati di avere le credenziali corrette per accedere al server FTP.
- Utilizza la modalità passiva (`-p`) se hai problemi di connessione a causa di firewall.
- Ricorda di disabilitare la modalità interattiva (`-i`) quando trasferisci molti file per evitare conferme manuali.