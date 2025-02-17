# [Linux] Bash sqlite3 utilizzo: Interagire con database SQLite

## Overview
Il comando `sqlite3` è uno strumento a riga di comando per interagire con i database SQLite. Permette di eseguire query SQL, gestire database e manipolare dati in modo semplice e diretto.

## Usage
La sintassi di base del comando `sqlite3` è la seguente:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Mostra un elenco delle opzioni disponibili.
- `-version`: Mostra la versione di SQLite in uso.
- `-init <file>`: Esegue i comandi SQL contenuti nel file specificato all'avvio.
- `-batch`: Esegue in modalità batch, utile per l'esecuzione di script senza interazione dell'utente.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `sqlite3`:

### Creare un nuovo database
```bash
sqlite3 mio_database.db
```

### Eseguire una query SQL
```bash
sqlite3 mio_database.db "SELECT * FROM utenti;"
```

### Creare una tabella
```bash
sqlite3 mio_database.db "CREATE TABLE utenti (id INTEGER PRIMARY KEY, nome TEXT, email TEXT);"
```

### Inserire dati in una tabella
```bash
sqlite3 mio_database.db "INSERT INTO utenti (nome, email) VALUES ('Mario Rossi', 'mario@example.com');"
```

### Esportare i dati in un file CSV
```bash
sqlite3 -header -csv mio_database.db "SELECT * FROM utenti;" > utenti.csv
```

## Tips
- Utilizza l'opzione `-init` per caricare automaticamente script SQL all'avvio di `sqlite3`.
- Ricorda di eseguire il backup del tuo database regolarmente per evitare perdite di dati.
- Sfrutta la modalità batch per automatizzare l'esecuzione di script SQL senza necessità di input manuale.