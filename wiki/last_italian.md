# [Linux] Bash last comando: visualizza gli accessi degli utenti

## Overview
Il comando `last` in Bash è utilizzato per visualizzare l'elenco degli accessi degli utenti al sistema. Mostra informazioni come il nome utente, l'ora di accesso, la durata della sessione e l'indirizzo IP o il nome dell'host da cui l'utente si è connesso.

## Usage
La sintassi di base del comando è la seguente:

```bash
last [opzioni] [argomenti]
```

## Common Options
- `-a`: Mostra l'indirizzo IP o il nome dell'host dell'utente.
- `-n [numero]`: Limita il numero di accessi visualizzati al numero specificato.
- `-R`: Non mostra il nome dell'host.
- `-x`: Mostra anche le informazioni sulle chiusure di sessione e i reboot.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `last`:

1. **Visualizzare tutti gli accessi recenti**:
   ```bash
   last
   ```

2. **Visualizzare gli accessi degli ultimi 5 utenti**:
   ```bash
   last -n 5
   ```

3. **Visualizzare gli accessi con indirizzo IP**:
   ```bash
   last -a
   ```

4. **Visualizzare gli accessi senza il nome dell'host**:
   ```bash
   last -R
   ```

5. **Visualizzare anche le chiusure di sessione e i reboot**:
   ```bash
   last -x
   ```

## Tips
- Usa `last -n 10` per controllare rapidamente gli ultimi 10 accessi, utile per un rapido audit.
- Puoi combinare diverse opzioni per ottenere informazioni più dettagliate, ad esempio `last -a -n 20` per vedere gli ultimi 20 accessi con indirizzi IP.
- Ricorda che `last` legge dal file `/var/log/wtmp`, quindi le informazioni potrebbero non essere disponibili se il file è stato ruotato o cancellato.