# [Linux] C Shell (csh) tee utilizzo: Duplica l'output in più file

## Overview
Il comando `tee` in C Shell (csh) è utilizzato per leggere dall'input standard e scrivere contemporaneamente sia sull'output standard che su uno o più file. Questo è utile quando si desidera visualizzare l'output di un comando e, allo stesso tempo, salvarlo per un uso futuro.

## Usage
La sintassi di base del comando `tee` è la seguente:

```csh
tee [options] [arguments]
```

## Common Options
- `-a`: Aggiunge l'output ai file esistenti invece di sovrascriverli.
- `-i`: Ignora i segnali di interruzione.
- `-p`: Stampa l'output su stdout e su file.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `tee`:

1. **Scrivere l'output di un comando in un file:**
   ```csh
   ls -l | tee file.txt
   ```
   Questo comando elenca i file nella directory corrente e scrive l'output nel file `file.txt`.

2. **Aggiungere l'output a un file esistente:**
   ```csh
   echo "Nuova riga" | tee -a file.txt
   ```
   Qui, la stringa "Nuova riga" viene aggiunta alla fine del file `file.txt`.

3. **Visualizzare l'output e scriverlo in più file:**
   ```csh
   echo "Testo di esempio" | tee file1.txt file2.txt
   ```
   Questo comando scrive "Testo di esempio" sia in `file1.txt` che in `file2.txt`, mostrando anche l'output sul terminale.

## Tips
- Utilizza l'opzione `-a` quando desideri mantenere il contenuto esistente di un file e aggiungere nuove informazioni.
- Ricorda che `tee` può essere utilizzato in pipeline, quindi puoi combinarlo con altri comandi per ottenere output più complessi.
- Se stai lavorando con file di log, `tee` è molto utile per monitorare l'output in tempo reale mentre lo registri.