# [Linux] Bash stat utilizzo: Visualizza informazioni sui file

## Overview
Il comando `stat` in Bash è utilizzato per visualizzare informazioni dettagliate sui file e sulle directory. Fornisce dati come la dimensione del file, le date di accesso e modifica, e i permessi di accesso.

## Usage
La sintassi di base del comando `stat` è la seguente:

```bash
stat [options] [arguments]
```

## Common Options
- `-c` : Specifica un formato personalizzato per l'output.
- `-f` : Mostra informazioni sul file system contenente il file.
- `--format` : Permette di definire un formato di output specifico.
- `-L` : Segue i link simbolici per mostrare le informazioni sul file originale.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `stat`:

1. Visualizzare informazioni di base su un file:
   ```bash
   stat nomefile.txt
   ```

2. Visualizzare informazioni su una directory:
   ```bash
   stat /percorso/della/directory
   ```

3. Usare un formato personalizzato per l'output:
   ```bash
   stat -c '%n: %s bytes' nomefile.txt
   ```

4. Mostrare informazioni sul file system di un file:
   ```bash
   stat -f nomefile.txt
   ```

5. Seguire i link simbolici:
   ```bash
   stat -L link_simbolico
   ```

## Tips
- Utilizza l'opzione `-c` per ottenere output più leggibili e personalizzati, specialmente quando lavori con script.
- Controlla le date di accesso e modifica per gestire i backup e le versioni dei file.
- Ricorda che `stat` può fornire informazioni utili anche per il debugging di problemi legati ai permessi di accesso ai file.