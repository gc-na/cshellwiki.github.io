# [Linux] Bash scp utilizzo: Copiare file in modo sicuro tra host

## Overview
Il comando `scp` (Secure Copy Protocol) è utilizzato per copiare file e directory in modo sicuro tra un computer locale e un computer remoto, o tra due computer remoti. Utilizza il protocollo SSH per garantire la sicurezza durante il trasferimento dei dati.

## Usage
La sintassi di base del comando `scp` è la seguente:

```bash
scp [opzioni] [origine] [destinazione]
```

## Common Options
Ecco alcune opzioni comuni per il comando `scp`:

- `-r`: Copia ricorsivamente le directory.
- `-P`: Specifica la porta da utilizzare per la connessione SSH (nota che è una maiuscola).
- `-i`: Specifica un file di chiave privata per l'autenticazione.
- `-v`: Abilita la modalità verbose, mostrando informazioni dettagliate sul processo di copia.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `scp`:

1. **Copiare un file dal computer locale a un server remoto:**
   ```bash
   scp /percorso/del/file.txt utente@server:/percorso/destinazione/
   ```

2. **Copiare un file da un server remoto al computer locale:**
   ```bash
   scp utente@server:/percorso/del/file.txt /percorso/destinazione/
   ```

3. **Copiare una directory intera in modo ricorsivo:**
   ```bash
   scp -r /percorso/della/directory utente@server:/percorso/destinazione/
   ```

4. **Copiare un file utilizzando una porta SSH specifica:**
   ```bash
   scp -P 2222 /percorso/del/file.txt utente@server:/percorso/destinazione/
   ```

5. **Copiare un file utilizzando una chiave privata:**
   ```bash
   scp -i /percorso/della/chiave_privata /percorso/del/file.txt utente@server:/percorso/destinazione/
   ```

## Tips
- Assicurati di avere i permessi necessari per accedere ai file e alle directory che stai copiando.
- Utilizza l'opzione `-v` per il debug se riscontri problemi durante il trasferimento.
- Se stai copiando file di grandi dimensioni, considera l'uso di `rsync` per un trasferimento più efficiente e ripetibile.