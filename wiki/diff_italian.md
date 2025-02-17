# [Linux] Bash diff utilizzo: confrontare file e directory

## Overview
Il comando `diff` è utilizzato per confrontare il contenuto di due file o directory, mostrando le differenze tra di essi. È uno strumento molto utile per gli sviluppatori e per chi lavora con il codice sorgente, poiché permette di identificare rapidamente le modifiche apportate.

## Usage
La sintassi di base del comando `diff` è la seguente:

```bash
diff [opzioni] [file1] [file2]
```

## Common Options
Ecco alcune delle opzioni più comuni per il comando `diff`:

- `-u`: Mostra le differenze in formato unificato, utile per la revisione del codice.
- `-i`: Ignora le differenze tra maiuscole e minuscole.
- `-w`: Ignora gli spazi bianchi durante il confronto.
- `-r`: Confronta ricorsivamente le directory.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `diff`:

### Esempio 1: Confrontare due file
```bash
diff file1.txt file2.txt
```
Questo comando mostrerà le differenze tra `file1.txt` e `file2.txt`.

### Esempio 2: Confrontare due file in formato unificato
```bash
diff -u file1.txt file2.txt
```
Utilizzando l'opzione `-u`, le differenze verranno visualizzate in un formato più leggibile.

### Esempio 3: Ignorare spazi bianchi
```bash
diff -w file1.txt file2.txt
```
Questo comando ignorerà le differenze dovute agli spazi bianchi.

### Esempio 4: Confrontare due directory
```bash
diff -r dir1/ dir2/
```
Con l'opzione `-r`, `diff` confronterà ricorsivamente tutti i file nelle directory `dir1` e `dir2`.

## Tips
- Quando si lavora con file di codice sorgente, utilizzare l'opzione `-u` per una visualizzazione più chiara delle modifiche.
- Se si confrontano file di testo, considerare di utilizzare l'opzione `-i` per ignorare le differenze di maiuscole e minuscole.
- Per confrontare directory, assicurarsi di utilizzare l'opzione `-r` per ottenere un confronto completo.