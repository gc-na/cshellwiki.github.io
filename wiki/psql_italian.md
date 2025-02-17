# [Linux] Bash psql Utilizzo: Esegui comandi SQL nel terminale

## Overview
Il comando `psql` è un'interfaccia a riga di comando per interagire con il database PostgreSQL. Permette agli utenti di eseguire query SQL, gestire database e amministrare il sistema direttamente dal terminale.

## Usage
La sintassi di base del comando `psql` è la seguente:

```bash
psql [options] [arguments]
```

## Common Options
- `-h`: Specifica l'host del server PostgreSQL.
- `-p`: Indica la porta su cui il server PostgreSQL è in ascolto.
- `-U`: Specifica il nome utente per la connessione al database.
- `-d`: Indica il nome del database a cui connettersi.
- `-c`: Esegue un comando SQL specificato e poi esce.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `psql`:

### Connessione a un database
```bash
psql -h localhost -U myuser -d mydatabase
```

### Esecuzione di una query SQL
```bash
psql -U myuser -d mydatabase -c "SELECT * FROM mytable;"
```

### Visualizzazione delle tabelle nel database
```bash
psql -U myuser -d mydatabase -c "\dt"
```

### Uscita dal prompt di psql
```bash
\q
```

## Tips
- Usa l'opzione `-W` per richiedere la password all'accesso.
- Puoi utilizzare il comando `\?` all'interno di psql per visualizzare un elenco di comandi disponibili.
- Salva le tue query in file `.sql` e eseguili con `psql -f nomefile.sql` per una gestione più semplice.