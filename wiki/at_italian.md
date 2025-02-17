# [Linux] Bash at Utilizzo: Pianificazione di comandi da eseguire in un momento specifico

## Overview
Il comando `at` consente di pianificare l'esecuzione di comandi o script in un momento specifico. È utile per automatizzare attività che devono essere eseguite una sola volta in futuro.

## Usage
La sintassi di base del comando `at` è la seguente:

```bash
at [opzioni] [tempo]
```

## Common Options
- `-f FILE`: Specifica un file contenente i comandi da eseguire.
- `-m`: Invia una mail all'utente anche se non ci sono output dal comando.
- `-q QUEUE`: Specifica una coda di lavoro per l'esecuzione.
- `-l`: Elenca i lavori programmati.
- `-d JOB_ID`: Cancella un lavoro programmato specificato dall'ID.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `at`:

1. **Pianificare un comando per eseguire in un'ora:**
   ```bash
   echo "echo 'Ciao, mondo!'" | at now + 1 hour
   ```

2. **Eseguire uno script in un giorno specifico:**
   ```bash
   at 14:00 2023-10-25 -f /path/to/script.sh
   ```

3. **Pianificare un comando per domani mattina:**
   ```bash
   echo "backup.sh" | at 9:00 tomorrow
   ```

4. **Elencare i lavori programmati:**
   ```bash
   at -l
   ```

5. **Cancellare un lavoro programmato:**
   ```bash
   at -d 2
   ```

## Tips
- Assicurati che il demone `atd` sia in esecuzione sul tuo sistema per utilizzare il comando `at`.
- Puoi utilizzare formati di data e ora flessibili, come "now + 5 minutes" o "next Monday".
- Controlla regolarmente i tuoi lavori programmati per evitare conflitti o sovrapposizioni.