# [Linux] Bash iotop utilizzo: Monitorare l'uso del disco in tempo reale

## Overview
Il comando `iotop` è uno strumento utile per monitorare l'uso del disco da parte dei processi in esecuzione su un sistema Linux. Mostra in tempo reale quali processi stanno generando la maggior parte delle operazioni di input/output (I/O) sul disco, permettendo agli utenti di identificare eventuali colli di bottiglia o problemi di prestazioni.

## Usage
La sintassi di base del comando `iotop` è la seguente:

```bash
iotop [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `iotop`:

- `-o`, `--only`: Mostra solo i processi che stanno attualmente effettuando operazioni di I/O.
- `-b`, `--batch`: Esegue `iotop` in modalità batch, utile per l'output su file o per l'analisi automatizzata.
- `-n NUM`, `--iter NUM`: Esegue `iotop` per un numero specifico di iterazioni prima di terminare.
- `-p PID`, `--pid=PID`: Monitora solo il processo con l'ID specificato.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `iotop`:

1. **Monitorare l'uso del disco in tempo reale**:
   ```bash
   iotop
   ```

2. **Visualizzare solo i processi attivi**:
   ```bash
   iotop -o
   ```

3. **Eseguire `iotop` in modalità batch per 10 iterazioni**:
   ```bash
   iotop -b -n 10
   ```

4. **Monitorare un processo specifico con PID 1234**:
   ```bash
   iotop -p 1234
   ```

## Tips
- Esegui `iotop` con i privilegi di root per ottenere informazioni complete sui processi.
- Usa la modalità batch se desideri registrare l'output in un file per analisi successive.
- Combina `iotop` con altri strumenti di monitoraggio per avere una visione più completa delle prestazioni del sistema.