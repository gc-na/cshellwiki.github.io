# [Linux] Bash source uso equivalente: Esegue comandi da un file

## Overview
Il comando `source` in Bash viene utilizzato per eseguire comandi contenuti in un file di script all'interno della shell corrente. Questo è particolarmente utile per caricare variabili d'ambiente o funzioni definite in un file senza dover avviare un nuovo processo di shell.

## Usage
La sintassi di base del comando `source` è la seguente:

```bash
source [opzioni] [file]
```

## Common Options
- `-`: Indica che il file deve essere eseguito in modo interattivo.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `--version`: Mostra la versione del comando.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `source`:

### Eseguire uno script
Per eseguire uno script chiamato `myscript.sh`:

```bash
source myscript.sh
```

### Caricare variabili d'ambiente
Se hai un file `env.sh` che definisce alcune variabili d'ambiente, puoi caricarle nella shell corrente:

```bash
source env.sh
```

### Usare con funzioni
Se hai definito delle funzioni in un file chiamato `functions.sh`, puoi caricarle per utilizzarle nella tua sessione:

```bash
source functions.sh
```

## Tips
- Assicurati che il file che stai cercando di eseguire abbia i permessi di lettura.
- Utilizza `source` invece di `./` per eseguire script se desideri che le variabili e le funzioni siano disponibili nella shell corrente.
- Controlla sempre il contenuto del file prima di eseguirlo per evitare l'esecuzione di comandi indesiderati.