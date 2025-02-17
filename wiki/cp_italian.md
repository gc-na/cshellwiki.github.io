# [Linux] Bash cp Utilizzo: Copiare file e directory

## Overview
Il comando `cp` in Bash è utilizzato per copiare file e directory da una posizione a un'altra. È uno strumento fondamentale per la gestione dei file nel sistema operativo Linux.

## Usage
La sintassi di base del comando `cp` è la seguente:

```bash
cp [opzioni] [origine] [destinazione]
```

## Common Options
Ecco alcune opzioni comuni per il comando `cp`:

- `-r`: Copia ricorsivamente le directory e il loro contenuto.
- `-i`: Chiede conferma prima di sovrascrivere un file esistente.
- `-u`: Copia solo se il file di origine è più recente del file di destinazione o se il file di destinazione non esiste.
- `-v`: Mostra i dettagli delle operazioni di copia eseguite.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `cp`:

1. **Copiare un file in un'altra posizione:**

   ```bash
   cp documento.txt /home/utente/documenti/
   ```

2. **Copiare una directory e il suo contenuto:**

   ```bash
   cp -r cartella_origine/ /home/utente/cartella_destinazione/
   ```

3. **Copiare un file chiedendo conferma prima di sovrascrivere:**

   ```bash
   cp -i documento.txt /home/utente/documenti/
   ```

4. **Copiare solo file più recenti:**

   ```bash
   cp -u documento.txt /home/utente/documenti/
   ```

5. **Copiare un file e visualizzare i dettagli:**

   ```bash
   cp -v documento.txt /home/utente/documenti/
   ```

## Tips
- Utilizza l'opzione `-i` per evitare di sovrascrivere accidentalmente file importanti.
- Quando copi file di grandi dimensioni o molte directory, considera l'uso dell'opzione `-v` per monitorare il progresso.
- Se stai copiando directory, assicurati di usare l'opzione `-r` per garantire che tutto il contenuto venga copiato correttamente.