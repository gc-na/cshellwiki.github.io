# [Linux] Bash uniq utilizzo: Rimuovere le righe duplicate

## Overview
Il comando `uniq` in Bash serve a rimuovere le righe duplicate da un file o da un input standard. È particolarmente utile quando si desidera ottenere un elenco di righe uniche da un file di testo.

## Usage
La sintassi di base del comando `uniq` è la seguente:

```bash
uniq [opzioni] [file]
```

Se non viene specificato alcun file, `uniq` legge dall'input standard.

## Common Options
Ecco alcune opzioni comuni per il comando `uniq`:

- `-c`: Conta il numero di occorrenze di ogni riga.
- `-d`: Mostra solo le righe duplicate.
- `-u`: Mostra solo le righe uniche.
- `-i`: Ignora la differenza tra maiuscole e minuscole.
- `-w N`: Confronta solo i primi N caratteri di ogni riga.

## Common Examples
Ecco alcuni esempi pratici dell'uso di `uniq`:

1. **Rimuovere righe duplicate da un file:**
   ```bash
   uniq file.txt
   ```

2. **Contare le righe duplicate:**
   ```bash
   uniq -c file.txt
   ```

3. **Mostrare solo le righe duplicate:**
   ```bash
   uniq -d file.txt
   ```

4. **Mostrare solo le righe uniche:**
   ```bash
   uniq -u file.txt
   ```

5. **Ignorare la differenza tra maiuscole e minuscole:**
   ```bash
   uniq -i file.txt
   ```

6. **Confrontare solo i primi 5 caratteri:**
   ```bash
   uniq -w 5 file.txt
   ```

## Tips
- Assicurati che il file di input sia ordinato prima di utilizzare `uniq`, poiché il comando funziona meglio su dati già ordinati.
- Puoi combinare `uniq` con altri comandi come `sort` per ottenere risultati più efficaci. Ad esempio:
  ```bash
  sort file.txt | uniq
  ```
- Usa l'opzione `-c` per avere un'idea di quante volte ogni riga appare nel tuo file, utile per analisi rapide.