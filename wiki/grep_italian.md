# [Linux] Bash grep utilizzo: Cerca testo in file

## Overview
Il comando `grep` è uno strumento potente utilizzato per cercare stringhe di testo all'interno di file. È particolarmente utile per filtrare l'output di altri comandi o per trovare informazioni specifiche in file di testo.

## Usage
La sintassi di base del comando `grep` è la seguente:

```bash
grep [opzioni] [pattern] [file]
```

## Common Options
Ecco alcune opzioni comuni per `grep`:

- `-i`: Ignora la distinzione tra maiuscole e minuscole.
- `-r`: Cerca ricorsivamente all'interno delle directory.
- `-v`: Inverte la ricerca, mostrando le righe che non corrispondono al pattern.
- `-n`: Mostra il numero di riga insieme alle righe trovate.
- `-l`: Elenca solo i nomi dei file che contengono il pattern.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `grep`:

1. **Cercare una parola in un file:**
   ```bash
   grep "parola" file.txt
   ```

2. **Cercare senza distinzione tra maiuscole e minuscole:**
   ```bash
   grep -i "parola" file.txt
   ```

3. **Cercare ricorsivamente in una directory:**
   ```bash
   grep -r "parola" /percorso/directory
   ```

4. **Mostrare le righe che non contengono il pattern:**
   ```bash
   grep -v "parola" file.txt
   ```

5. **Mostrare il numero di riga delle corrispondenze:**
   ```bash
   grep -n "parola" file.txt
   ```

## Tips
- Usa `grep` in combinazione con altri comandi tramite pipe per filtrare l'output, ad esempio: `dmesg | grep "errore"`.
- Se stai cercando in file di grandi dimensioni, considera l'uso dell'opzione `-m` per limitare il numero di corrispondenze restituite.
- Ricorda di utilizzare le virgolette per i pattern che contengono spazi o caratteri speciali.