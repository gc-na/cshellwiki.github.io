# [Linux] C Shell (csh) sqlite3 Utilizzo: Interagire con database SQLite

## Overview
Il comando `sqlite3` è un'interfaccia a riga di comando per interagire con i database SQLite. Permette di eseguire query SQL, gestire database e manipolare dati in modo semplice e diretto.

## Usage
La sintassi di base del comando `sqlite3` è la seguente:

```bash
sqlite3 [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `sqlite3`:

- `-header`: Mostra i nomi delle colonne nell'output.
- `-csv`: Esporta i risultati in formato CSV.
- `-init <file>`: Esegue comandi SQL da un file all'avvio.
- `-batch`: Esegue in modalità batch, utile per script.
- `-version`: Mostra la versione di SQLite in uso.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `sqlite3`:

1. **Creare un nuovo database:**
   ```bash
   sqlite3 nuovo_database.db
   ```

2. **Eseguire una query SQL:**
   ```bash
   sqlite3 nuovo_database.db "SELECT * FROM tabella;"
   ```

3. **Importare dati da un file CSV:**
   ```bash
   sqlite3 -csv nuovo_database.db ".import dati.csv tabella"
   ```

4. **Esportare dati in formato CSV:**
   ```bash
   sqlite3 -header -csv nuovo_database.db "SELECT * FROM tabella;" > output.csv
   ```

5. **Eseguire comandi da un file SQL:**
   ```bash
   sqlite3 nuovo_database.db < script.sql
   ```

## Tips
- Utilizza l'opzione `-header` per rendere l'output più leggibile.
- Fai sempre un backup del tuo database prima di eseguire operazioni di modifica.
- Sperimenta con la modalità batch per automatizzare le operazioni ripetitive.
- Controlla la versione di SQLite per assicurarti di utilizzare le funzionalità più recenti.