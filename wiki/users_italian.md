# [Linux] Bash users utilizzo: Visualizza gli utenti attivi

## Overview
Il comando `users` in Bash è utilizzato per visualizzare gli utenti attualmente connessi al sistema. Mostra semplicemente i nomi degli utenti che hanno una sessione attiva.

## Usage
La sintassi di base del comando è la seguente:

```bash
users [options]
```

## Common Options
- `-n`: Mostra solo il numero di utenti connessi.
- `-r`: Mostra solo gli utenti che sono stati connessi come root.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `users`:

1. **Visualizzare gli utenti attivi:**
   ```bash
   users
   ```

2. **Contare il numero di utenti connessi:**
   ```bash
   users -n
   ```

3. **Visualizzare solo gli utenti root:**
   ```bash
   users -r
   ```

## Tips
- Utilizza `who` o `w` per ottenere informazioni più dettagliate sugli utenti connessi, come l'orario di accesso e l'attività attuale.
- Se desideri monitorare gli accessi in tempo reale, considera di utilizzare `watch users` per aggiornare automaticamente l'output.