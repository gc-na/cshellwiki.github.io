# [Linux] Bash umask utilizzo: Imposta i permessi predefiniti per i nuovi file e directory

## Overview
Il comando `umask` in Bash viene utilizzato per impostare i permessi predefiniti per i nuovi file e directory creati dagli utenti. La maschera di umask determina quali permessi verranno negati quando vengono creati nuovi file o directory, influenzando quindi la sicurezza e l'accesso ai file.

## Usage
La sintassi di base del comando `umask` è la seguente:

```bash
umask [opzioni] [argomenti]
```

## Common Options
- `-S`: Mostra la maschera di umask in forma simbolica.
- `-p`: Mostra la maschera di umask corrente in modo persistente.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `umask`:

1. **Visualizzare la maschera umask corrente:**

   ```bash
   umask
   ```

2. **Impostare una nuova maschera umask:**

   ```bash
   umask 027
   ```

   Questo comando imposta i permessi predefiniti in modo che il proprietario abbia tutti i permessi, il gruppo abbia solo i permessi di lettura ed esecuzione, e gli altri non abbiano alcun permesso.

3. **Visualizzare la maschera umask in forma simbolica:**

   ```bash
   umask -S
   ```

4. **Impostare una maschera umask simbolica:**

   ```bash
   umask u=rwx,g=rx,o=
   ```

   Questo comando imposta i permessi per il proprietario, il gruppo e gli altri in modo specifico.

## Tips
- È consigliabile controllare la maschera umask prima di creare file sensibili per garantire che i permessi siano appropriati.
- Puoi aggiungere il comando `umask` nel tuo file di configurazione della shell (come `.bashrc` o `.bash_profile`) per impostare automaticamente i permessi desiderati all'avvio della sessione.
- Ricorda che i permessi di umask sono sottratti dai permessi predefiniti (664 per i file e 775 per le directory).