# [Linux] C Shell (csh) systemctl uso: Gestire i servizi di sistema

## Overview
Il comando `systemctl` è uno strumento fondamentale per gestire i servizi di sistema su sistemi operativi basati su systemd. Permette di avviare, fermare, riavviare e controllare lo stato dei servizi, facilitando la gestione delle applicazioni e dei demoni in esecuzione.

## Usage
La sintassi di base del comando `systemctl` è la seguente:

```bash
systemctl [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `systemctl` con brevi spiegazioni:

- `start`: Avvia un servizio.
- `stop`: Ferma un servizio.
- `restart`: Riavvia un servizio.
- `status`: Mostra lo stato di un servizio.
- `enable`: Abilita un servizio all'avvio del sistema.
- `disable`: Disabilita un servizio all'avvio del sistema.
- `list-units`: Elenca tutte le unità attive.

## Common Examples
Di seguito sono riportati alcuni esempi pratici dell'uso di `systemctl`:

### Avviare un servizio
```bash
systemctl start nome_servizio
```

### Fermare un servizio
```bash
systemctl stop nome_servizio
```

### Riavviare un servizio
```bash
systemctl restart nome_servizio
```

### Controllare lo stato di un servizio
```bash
systemctl status nome_servizio
```

### Abilitare un servizio all'avvio
```bash
systemctl enable nome_servizio
```

### Disabilitare un servizio all'avvio
```bash
systemctl disable nome_servizio
```

### Elencare tutte le unità attive
```bash
systemctl list-units --type=service
```

## Tips
- Assicurati di avere i permessi necessari per eseguire `systemctl`, spesso è richiesto l'accesso come superutente.
- Usa `systemctl status` per diagnosticare problemi con i servizi, poiché fornisce informazioni dettagliate sui log.
- Ricorda di abilitare i servizi che desideri far partire automaticamente all'avvio del sistema per evitare di doverli avviare manualmente ogni volta.