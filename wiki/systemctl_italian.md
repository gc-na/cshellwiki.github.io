# [Linux] Bash systemctl utilizzo: Gestire i servizi di sistema

## Overview
Il comando `systemctl` è uno strumento fondamentale per interagire con il sistema di init systemd. Permette di controllare e gestire i servizi di sistema, le unità e le configurazioni, facilitando l'amministrazione del sistema operativo.

## Usage
La sintassi di base del comando `systemctl` è la seguente:

```bash
systemctl [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `systemctl`:

- `start`: Avvia un'unità (servizio).
- `stop`: Ferma un'unità.
- `restart`: Riavvia un'unità.
- `status`: Mostra lo stato di un'unità.
- `enable`: Abilita un'unità per l'avvio automatico all'avvio del sistema.
- `disable`: Disabilita un'unità dall'avvio automatico.
- `list-units`: Elenca le unità attive.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `systemctl`:

- Avviare un servizio:
  ```bash
  systemctl start nome_servizio
  ```

- Fermare un servizio:
  ```bash
  systemctl stop nome_servizio
  ```

- Riavviare un servizio:
  ```bash
  systemctl restart nome_servizio
  ```

- Controllare lo stato di un servizio:
  ```bash
  systemctl status nome_servizio
  ```

- Abilitare un servizio all'avvio:
  ```bash
  systemctl enable nome_servizio
  ```

- Disabilitare un servizio dall'avvio:
  ```bash
  systemctl disable nome_servizio
  ```

- Elencare tutte le unità attive:
  ```bash
  systemctl list-units
  ```

## Tips
- Assicurati di avere i permessi necessari (spesso è richiesto l'uso di `sudo`) per eseguire comandi `systemctl` che modificano lo stato dei servizi.
- Utilizza `systemctl list-units --type=service` per filtrare e visualizzare solo i servizi.
- Controlla i log di un'unità con `journalctl -u nome_servizio` per diagnosticare problemi.