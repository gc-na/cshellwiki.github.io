# [Linux] Bash strace utilizzo: Strumento per il tracciamento delle chiamate di sistema

## Overview
Il comando `strace` è uno strumento potente utilizzato per monitorare e diagnosticare le chiamate di sistema effettuate da un programma in esecuzione. Permette di vedere quali file vengono aperti, quali segnali vengono ricevuti e quali errori si verificano, rendendolo utile per il debug delle applicazioni.

## Usage
La sintassi di base del comando `strace` è la seguente:

```bash
strace [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per `strace` con brevi spiegazioni:

- `-o <file>`: Scrive l'output in un file specificato invece di stampare sul terminale.
- `-e <expression>`: Filtra le chiamate di sistema da tracciare in base a un'espressione specificata.
- `-p <pid>`: Attacca un processo esistente identificato dal suo PID (Process ID).
- `-c`: Riporta un riepilogo delle statistiche delle chiamate di sistema al termine dell'esecuzione.
- `-f`: Segue i processi figli creati durante l'esecuzione del programma.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `strace`:

1. Tracciare un comando semplice:
   ```bash
   strace ls
   ```

2. Scrivere l'output in un file:
   ```bash
   strace -o output.txt ls
   ```

3. Tracciare solo le chiamate di sistema relative ai file:
   ```bash
   strace -e trace=file ls
   ```

4. Attaccare un processo esistente:
   ```bash
   strace -p 1234
   ```

5. Ottenere un riepilogo delle statistiche delle chiamate di sistema:
   ```bash
   strace -c ls
   ```

## Tips
- Utilizza l'opzione `-o` per salvare l'output in un file se stai analizzando molte informazioni.
- Filtra le chiamate di sistema con `-e` per concentrarti su ciò che è rilevante per il tuo debug.
- Ricorda che `strace` può rallentare l'esecuzione del programma, quindi usalo principalmente in ambienti di sviluppo o test.
- Se stai tracciando un processo che crea altri processi, usa l'opzione `-f` per seguire anche i processi figli.