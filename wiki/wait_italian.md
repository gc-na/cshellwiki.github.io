# [Linux] Bash wait utilizzo: Attendere il completamento di un processo

## Overview
Il comando `wait` in Bash è utilizzato per attendere il completamento di uno o più processi in background. Quando viene eseguito, il terminale rimane in attesa fino a quando il processo specificato non termina, restituendo il suo stato di uscita.

## Usage
La sintassi di base del comando `wait` è la seguente:

```bash
wait [options] [arguments]
```

## Common Options
- `-n`: Attende il completamento di qualsiasi processo in background.
- `-p`: Attende il completamento di un processo specifico e restituisce il suo stato di uscita.
- `PID`: Specifica l'ID del processo di cui si desidera attendere il completamento.

## Common Examples

### Esempio 1: Attendere un processo specifico
```bash
sleep 5 &
PID=$!
wait $PID
echo "Il processo con PID $PID è terminato."
```
In questo esempio, il comando `sleep 5` viene eseguito in background e il terminale attende la sua conclusione.

### Esempio 2: Attendere più processi
```bash
sleep 3 &
sleep 5 &
wait
echo "Tutti i processi in background sono terminati."
```
Qui, entrambi i comandi `sleep` vengono eseguiti in background e il terminale attende che entrambi siano completati.

### Esempio 3: Utilizzare l'opzione -n
```bash
sleep 2 &
sleep 4 &
wait -n
echo "Un processo in background è terminato."
```
In questo caso, il terminale attende che uno dei due processi in background termini, senza aspettare che tutti siano completati.

## Tips
- Utilizza `wait` in script per sincronizzare processi in background e garantire che le operazioni dipendenti siano eseguite solo dopo il completamento dei processi richiesti.
- Ricorda di salvare l'ID del processo (PID) se desideri attendere un processo specifico.
- Se non specifichi alcun PID, `wait` attenderà il completamento di tutti i processi in background attivi.