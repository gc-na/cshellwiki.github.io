# [Linux] Bash nice utilizzo: Modifica la priorità dei processi

## Overview
Il comando `nice` in Bash viene utilizzato per avviare un processo con una priorità modificata. Questo è utile per gestire l'uso delle risorse del sistema, consentendo di dare più o meno importanza a determinati processi rispetto ad altri.

## Usage
La sintassi di base del comando è la seguente:

```bash
nice [opzioni] [comando]
```

## Common Options
- `-n`, `--adjustment`: Specifica il valore di aggiustamento della priorità. Può essere un numero intero da -20 (priorità massima) a 19 (priorità minima).
- `-h`, `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `-v`, `--version`: Mostra la versione del comando `nice`.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `nice`:

1. **Eseguire un comando con priorità normale:**
   ```bash
   nice comando
   ```

2. **Eseguire un comando con priorità più bassa:**
   ```bash
   nice -n 10 comando
   ```

3. **Eseguire un processo con priorità alta:**
   ```bash
   nice -n -5 comando
   ```

4. **Controllare la priorità di un processo in esecuzione:**
   ```bash
   ps -o pid,ni,cmd
   ```

## Tips
- Utilizza valori negativi per aumentare la priorità di un processo importante, ma fai attenzione a non sovraccaricare il sistema.
- Controlla sempre la priorità dei processi in esecuzione con `ps` per evitare conflitti di risorse.
- Ricorda che solo l'utente root può impostare priorità negative. Gli utenti normali possono solo aumentare il valore di nice (ridurre la priorità).