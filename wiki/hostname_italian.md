# [Linux] Bash hostname utilizzo: Ottieni o imposta il nome dell'host

## Overview
Il comando `hostname` in Bash viene utilizzato per visualizzare o impostare il nome dell'host del sistema. Il nome dell'host è un identificatore unico per un dispositivo all'interno di una rete, facilitando la comunicazione tra i vari dispositivi.

## Usage
La sintassi di base del comando è la seguente:

```bash
hostname [options] [arguments]
```

## Common Options
- `-a`, `--alias`: Mostra il nome alias dell'host.
- `-d`, `--domain`: Mostra il nome del dominio dell'host.
- `-f`, `--fqdn`: Mostra il nome di dominio completamente qualificato (FQDN).
- `-i`, `--ip-address`: Mostra l'indirizzo IP dell'host.
- `-s`, `--short`: Mostra solo il nome breve dell'host.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `hostname`:

1. **Visualizzare il nome dell'host corrente:**
   ```bash
   hostname
   ```

2. **Visualizzare il nome di dominio completamente qualificato:**
   ```bash
   hostname -f
   ```

3. **Visualizzare l'indirizzo IP dell'host:**
   ```bash
   hostname -i
   ```

4. **Impostare un nuovo nome per l'host:**
   ```bash
   sudo hostname nuovo-nome-host
   ```

5. **Visualizzare solo il nome breve dell'host:**
   ```bash
   hostname -s
   ```

## Tips
- Assicurati di avere i permessi necessari (solitamente come utente root) per modificare il nome dell'host.
- Dopo aver cambiato il nome dell'host, potrebbe essere necessario riavviare il sistema o riavviare i servizi di rete per applicare le modifiche.
- Controlla sempre il nome dell'host dopo aver effettuato modifiche per confermare che siano state applicate correttamente.