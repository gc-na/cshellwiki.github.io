# [Linux] Bash find utilizzo: trova nomi di file

## Overview
Il comando `find` è uno strumento potente utilizzato per cercare file e directory all'interno di una gerarchia di directory. Permette di specificare vari criteri di ricerca, come il nome del file, la dimensione, la data di modifica e altro ancora.

## Usage
La sintassi di base del comando `find` è la seguente:

```bash
find [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `find`:

- `-name`: cerca file con un nome specifico.
- `-type`: filtra i risultati in base al tipo di file (ad esempio, `f` per file regolari, `d` per directory).
- `-size`: cerca file in base alla loro dimensione.
- `-mtime`: cerca file in base alla data di modifica (es. `-mtime -7` per file modificati negli ultimi 7 giorni).
- `-exec`: esegue un comando su ogni file trovato.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `find`:

1. **Cercare un file per nome**:
   ```bash
   find /percorso/directory -name "esempio.txt"
   ```

2. **Cercare tutte le directory**:
   ```bash
   find /percorso/directory -type d
   ```

3. **Cercare file di una certa dimensione**:
   ```bash
   find /percorso/directory -size +10M
   ```

4. **Cercare file modificati negli ultimi 30 giorni**:
   ```bash
   find /percorso/directory -mtime -30
   ```

5. **Eseguire un comando su file trovati**:
   ```bash
   find /percorso/directory -name "*.log" -exec rm {} \;
   ```

## Tips
- Utilizza le opzioni `-print` per visualizzare i risultati della ricerca in modo esplicito.
- Fai attenzione quando usi `-exec`, specialmente con comandi che modificano o eliminano file.
- Puoi combinare più criteri di ricerca usando le opzioni logiche come `-and` e `-or` per affinare ulteriormente i risultati.