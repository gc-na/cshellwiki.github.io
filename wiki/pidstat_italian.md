# [Linux] Bash pidstat Uso: Monitoraggio delle statistiche dei processi

## Overview
Il comando `pidstat` è uno strumento utile per monitorare le statistiche delle prestazioni dei processi in esecuzione su un sistema Linux. Fornisce informazioni dettagliate sull'utilizzo della CPU, della memoria e di altre risorse per ogni processo, consentendo agli amministratori di sistema e agli utenti di analizzare il comportamento delle applicazioni.

## Usage
La sintassi di base del comando `pidstat` è la seguente:

```bash
pidstat [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `pidstat` con brevi spiegazioni:

- `-p <pid>`: Specifica il PID (Process ID) del processo da monitorare.
- `-r`: Mostra l'utilizzo della memoria.
- `-u`: Mostra l'utilizzo della CPU.
- `-h`: Mostra l'output in un formato leggibile (senza scienziato).
- `-t`: Mostra le statistiche per i thread del processo.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `pidstat`:

1. **Monitorare l'utilizzo della CPU per tutti i processi:**

   ```bash
   pidstat -u
   ```

2. **Monitorare un processo specifico con PID 1234:**

   ```bash
   pidstat -p 1234
   ```

3. **Visualizzare l'utilizzo della memoria per tutti i processi:**

   ```bash
   pidstat -r
   ```

4. **Monitorare l'utilizzo della CPU e della memoria ogni 2 secondi:**

   ```bash
   pidstat -u -r 2
   ```

5. **Mostrare le statistiche per i thread di un processo specifico:**

   ```bash
   pidstat -t -p 1234
   ```

## Tips
- Utilizza l'opzione `-h` per rendere l'output più leggibile, specialmente quando lavori con grandi numeri.
- Combina le opzioni per ottenere informazioni più dettagliate, come l'utilizzo della CPU e della memoria insieme.
- Esegui `pidstat` in un terminale separato mentre stai testando o monitorando un'applicazione per ottenere dati in tempo reale.