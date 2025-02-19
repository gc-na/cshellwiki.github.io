# [Linux] C Shell (csh) ftp utilizzo: Trasferimento di file tra computer

## Overview
Il comando `ftp` (File Transfer Protocol) è utilizzato per trasferire file tra computer su una rete. Permette di connettersi a un server FTP e di eseguire operazioni come il caricamento e il download di file.

## Usage
La sintassi di base del comando `ftp` è la seguente:

```csh
ftp [opzioni] [argomenti]
```

## Common Options
- `-i`: Disabilita il trasferimento in modalità interattiva.
- `-n`: Non tenta di effettuare il login automaticamente.
- `-v`: Abilita la modalità verbosa, mostrando più dettagli durante il trasferimento.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `ftp`:

### Connessione a un server FTP
```csh
ftp ftp.example.com
```

### Download di un file
```csh
get nomefile.txt
```

### Upload di un file
```csh
put nomefile.txt
```

### Visualizzazione della lista dei file
```csh
ls
```

### Disconnessione dal server
```csh
bye
```

## Tips
- Utilizza l'opzione `-i` per velocizzare il trasferimento di file di grandi dimensioni, evitando conferme per ogni file.
- Assicurati di avere i permessi necessari per caricare o scaricare file dal server FTP.
- Ricorda di disconnetterti correttamente dal server usando il comando `bye` per evitare sessioni aperte.