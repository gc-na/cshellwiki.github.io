# [Linux] Bash journalctl utilizzo: Visualizzare i log di sistema

## Overview
Il comando `journalctl` è utilizzato per visualizzare i log del sistema registrati dal sistema di logging `systemd`. Permette agli utenti di accedere a informazioni dettagliate sui messaggi di log generati dai vari servizi e dal kernel, facilitando la diagnostica e la risoluzione dei problemi.

## Usage
La sintassi di base del comando è la seguente:

```bash
journalctl [options] [arguments]
```

## Common Options
- `-b`: Mostra i log dall'ultimo avvio del sistema.
- `-f`: Segue i log in tempo reale, simile a `tail -f`.
- `--since`: Filtra i log a partire da una data/ora specifica.
- `--until`: Filtra i log fino a una data/ora specifica.
- `-u <unit>`: Mostra i log per una specifica unità di sistema (servizio).
- `-p <priority>`: Filtra i log in base alla priorità (es. `err`, `warning`, `info`).

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `journalctl`:

1. **Visualizzare tutti i log:**
   ```bash
   journalctl
   ```

2. **Visualizzare i log dall'ultimo avvio:**
   ```bash
   journalctl -b
   ```

3. **Seguire i log in tempo reale:**
   ```bash
   journalctl -f
   ```

4. **Visualizzare i log di un'unità specifica:**
   ```bash
   journalctl -u ssh.service
   ```

5. **Filtrare i log per data:**
   ```bash
   journalctl --since "2023-10-01" --until "2023-10-10"
   ```

6. **Visualizzare solo i log di errore:**
   ```bash
   journalctl -p err
   ```

## Tips
- Utilizza `-f` per monitorare i log in tempo reale durante la risoluzione dei problemi.
- Combina `--since` e `--until` per analizzare i log in un intervallo di tempo specifico.
- Ricorda che i log possono occupare molto spazio; considera di pulirli regolarmente con `journalctl --vacuum-time=2weeks` per mantenere solo i log degli ultimi due settimane.