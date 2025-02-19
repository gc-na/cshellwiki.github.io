# [Linux] C Shell (csh) docker utilizzo: Gestire contenitori e immagini

## Overview
Il comando `docker` è uno strumento potente per gestire contenitori e immagini in un ambiente di virtualizzazione. Permette di creare, eseguire e gestire applicazioni in contenitori isolati, facilitando lo sviluppo e il deployment.

## Usage
La sintassi di base del comando `docker` è la seguente:

```csh
docker [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni utilizzate con il comando `docker`:

- `run`: Esegue un nuovo contenitore.
- `ps`: Mostra i contenitori in esecuzione.
- `images`: Elenca le immagini disponibili localmente.
- `rmi`: Rimuove un'immagine.
- `exec`: Esegue un comando in un contenitore in esecuzione.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `docker`:

1. **Eseguire un nuovo contenitore**:
   ```csh
   docker run hello-world
   ```

2. **Elencare i contenitori in esecuzione**:
   ```csh
   docker ps
   ```

3. **Elencare tutte le immagini disponibili**:
   ```csh
   docker images
   ```

4. **Rimuovere un'immagine**:
   ```csh
   docker rmi nome_immagine
   ```

5. **Eseguire un comando in un contenitore esistente**:
   ```csh
   docker exec -it nome_contenitore bash
   ```

## Tips
- Assicurati di avere i permessi necessari per eseguire i comandi `docker`, potresti dover utilizzare `sudo` in alcune configurazioni.
- Utilizza `docker-compose` per gestire applicazioni multi-contenitore in modo più semplice.
- Mantieni le tue immagini aggiornate per sfruttare le ultime funzionalità e correzioni di sicurezza.