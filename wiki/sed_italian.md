# [Linux] Bash sed Uso: Modifica e trasforma il testo

## Overview
Il comando `sed` (stream editor) è uno strumento potente in Bash utilizzato per modificare e trasformare il testo in modo non interattivo. È particolarmente utile per l'elaborazione di file di testo e per l'automazione di compiti ripetitivi.

## Usage
La sintassi di base del comando `sed` è la seguente:

```bash
sed [opzioni] [argomenti]
```

## Common Options
- `-e`: Permette di specificare un'espressione di editing.
- `-i`: Modifica i file in modo "in-place", ovvero direttamente nel file originale.
- `-n`: Sopprime l'output predefinito, mostrando solo le righe specificate.
- `s/pattern/replacement/`: Sostituisce il `pattern` con `replacement` in ogni riga.

## Common Examples
Ecco alcuni esempi pratici dell'uso di `sed`:

1. **Sostituire una parola in un file**:
   ```bash
   sed 's/vecchia_parola/nuova_parola/' file.txt
   ```

2. **Modificare un file direttamente**:
   ```bash
   sed -i 's/vecchia_parola/nuova_parola/' file.txt
   ```

3. **Stampare solo le righe che contengono un certo pattern**:
   ```bash
   sed -n '/pattern/p' file.txt
   ```

4. **Eliminare le righe vuote da un file**:
   ```bash
   sed '/^$/d' file.txt
   ```

5. **Aggiungere una stringa all'inizio di ogni riga**:
   ```bash
   sed 's/^/stringa_da_aggiungere/' file.txt
   ```

## Tips
- Utilizza l'opzione `-i` con cautela, poiché modifica il file originale. È consigliabile fare una copia di backup prima di eseguire modifiche in-place.
- Sperimenta con l'opzione `-n` per controllare quali righe vengono stampate e per affinare le tue espressioni `sed`.
- Le espressioni regolari sono potenti; impara a usarle per ottenere risultati più complessi e precisi.