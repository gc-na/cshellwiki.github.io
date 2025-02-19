# [Linux] C Shell (csh) stat Uso: visualizza informazioni sui file

## Overview
Il comando `stat` in C Shell (csh) viene utilizzato per visualizzare informazioni dettagliate sui file e sulle directory. Fornisce dati come la dimensione del file, le date di accesso e modifica, e i permessi di accesso.

## Usage
La sintassi di base del comando `stat` è la seguente:

```csh
stat [options] [arguments]
```

## Common Options
- `-c`: Specifica un formato di output personalizzato.
- `-f`: Mostra informazioni in un formato compatto.
- `-L`: Segue i link simbolici per mostrare le informazioni sul file di destinazione.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `stat`:

1. **Visualizzare informazioni di base su un file:**
   ```csh
   stat nomefile.txt
   ```

2. **Utilizzare un formato personalizzato per l'output:**
   ```csh
   stat -c "%s bytes" nomefile.txt
   ```

3. **Mostrare informazioni su un link simbolico seguendo il link:**
   ```csh
   stat -L link_simbolico
   ```

4. **Visualizzare informazioni in un formato compatto:**
   ```csh
   stat -f "%N %z" nomefile.txt
   ```

## Tips
- Utilizza l'opzione `-c` per personalizzare l'output secondo le tue esigenze, rendendo più facile la lettura delle informazioni.
- Se stai lavorando con link simbolici, ricorda di usare l'opzione `-L` per ottenere informazioni sul file reale.
- Controlla sempre i permessi di accesso e le date di modifica per gestire correttamente i file nel tuo sistema.