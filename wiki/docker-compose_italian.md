# [Linux] Bash docker-compose utilizzo: Gestire applicazioni Docker multi-contenitore

## Overview
Il comando `docker-compose` è uno strumento per definire e gestire applicazioni Docker che consistono in più contenitori. Utilizzando un file di configurazione, è possibile specificare i servizi, le reti e i volumi necessari per l'applicazione, semplificando così il processo di avvio e gestione.

## Usage
La sintassi di base del comando `docker-compose` è la seguente:

```bash
docker-compose [opzioni] [argomenti]
```

## Common Options
- `up`: Avvia i contenitori definiti nel file `docker-compose.yml`.
- `down`: Ferma e rimuove i contenitori, le reti e i volumi creati da `up`.
- `build`: Costruisce o ricostruisce i servizi.
- `logs`: Mostra i log dei contenitori.
- `ps`: Elenca i contenitori in esecuzione.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `docker-compose`:

### Avviare i contenitori
```bash
docker-compose up
```

### Avviare i contenitori in modalità staccata
```bash
docker-compose up -d
```

### Fermare i contenitori
```bash
docker-compose down
```

### Costruire i servizi
```bash
docker-compose build
```

### Visualizzare i log dei contenitori
```bash
docker-compose logs
```

### Elencare i contenitori in esecuzione
```bash
docker-compose ps
```

## Tips
- Utilizza il flag `-d` con `up` per eseguire i contenitori in background, permettendo di continuare a utilizzare il terminale.
- Assicurati di avere un file `docker-compose.yml` ben configurato per evitare errori durante l'avvio dei servizi.
- Usa `docker-compose exec [servizio] [comando]` per eseguire comandi all'interno di un contenitore in esecuzione.