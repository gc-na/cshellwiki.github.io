# [Linux] C Shell (csh) strace Uso: Strumenti di tracciamento delle chiamate di sistema

## Overview
Il comando `strace` è uno strumento potente utilizzato per monitorare e diagnosticare le chiamate di sistema effettuate da un programma in esecuzione. Permette di vedere quali file vengono aperti, quali segnali vengono ricevuti e altre interazioni con il sistema operativo.

## Usage
La sintassi di base del comando `strace` è la seguente:

```bash
strace [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per `strace`:

- `-c`: Riporta un riepilogo delle statistiche delle chiamate di sistema.
- `-e trace=<syscall>`: Traccia solo le chiamate di sistema specificate.
- `-o <file>`: Scrive l'output in un file invece di stamparlo sullo schermo.
- `-p <pid>`: Attacca un processo in esecuzione specificato dal suo PID.

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

3. Tracciare solo le chiamate di sistema di apertura file:
   ```bash
   strace -e trace=open ls
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
- Utilizza l'opzione `-o` per salvare l'output in un file quando tracci un programma lungo, per facilitare l'analisi successiva.
- Fai attenzione all'uso di `strace` su processi di produzione, poiché può influenzare le prestazioni.
- Combina `strace` con altre utilità come `grep` per filtrare l'output e trovare rapidamente le informazioni necessarie.