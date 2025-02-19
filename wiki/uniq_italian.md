# [Linux] C Shell (csh) uniq Utilizzo: Rimuovere righe duplicate da un file

## Overview
Il comando `uniq` in C Shell (csh) viene utilizzato per rimuovere righe duplicate da un file o da un input standard. È particolarmente utile quando si desidera ottenere un elenco di elementi unici da un file di testo.

## Usage
La sintassi di base del comando è la seguente:

```
uniq [options] [arguments]
```

## Common Options
- `-c`: Conta il numero di occorrenze di ciascuna riga.
- `-d`: Mostra solo le righe duplicate.
- `-u`: Mostra solo le righe uniche.
- `-i`: Ignora la differenza tra maiuscole e minuscole.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `uniq`:

1. Rimuovere righe duplicate da un file:
   ```csh
   uniq file.txt
   ```

2. Contare le occorrenze di ciascuna riga:
   ```csh
   uniq -c file.txt
   ```

3. Mostrare solo le righe duplicate:
   ```csh
   uniq -d file.txt
   ```

4. Mostrare solo le righe uniche:
   ```csh
   uniq -u file.txt
   ```

5. Ignorare la differenza tra maiuscole e minuscole:
   ```csh
   uniq -i file.txt
   ```

## Tips
- Assicurati che il file di input sia ordinato prima di utilizzare `uniq`, poiché il comando funziona meglio su dati già ordinati.
- Puoi combinare `uniq` con altri comandi come `sort` per ottenere risultati più efficaci. Ad esempio:
  ```csh
  sort file.txt | uniq
  ```
- Utilizza l'opzione `-c` per avere un'idea di quante volte ogni riga appare nel file, utile per analisi rapide.