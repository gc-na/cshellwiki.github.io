# [Linux] Bash @ uso: [eseguire comandi in background]

## Overview
Il comando `@` in Bash è utilizzato per eseguire comandi in background, permettendo all'utente di continuare a utilizzare il terminale mentre il comando viene eseguito. Questo è particolarmente utile per processi lunghi o per eseguire più comandi contemporaneamente.

## Usage
La sintassi di base del comando è la seguente:

```bash
@ [opzioni] [argomenti]
```

## Common Options
- `&` : Esegue il comando in background.
- `disown` : Rimuove il comando in background dalla lista dei job, permettendo di chiudere il terminale senza terminare il processo.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `@`:

1. Eseguire un comando in background:
   ```bash
   sleep 30 &
   ```
   Questo comando esegue `sleep 30` in background, permettendo di continuare a usare il terminale.

2. Eseguire più comandi in background:
   ```bash
   wget http://example.com/file.zip &
   tar -xzf file.zip &
   ```
   Qui, `wget` scarica un file mentre `tar` lo estrae, entrambi in background.

3. Usare `disown` per mantenere un processo attivo dopo la chiusura del terminale:
   ```bash
   long_running_command &
   disown
   ```
   Questo comando esegue `long_running_command` in background e lo rimuove dalla lista dei job.

## Tips
- Usa `jobs` per visualizzare i processi in background attivi.
- Se vuoi portare un processo in primo piano, usa il comando `fg`.
- Ricorda che i processi in background continueranno a funzionare anche se chiudi il terminale, a meno che non li disowni.