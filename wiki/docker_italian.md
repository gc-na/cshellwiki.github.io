# [Linux] Bash docker uso: Gestire container e immagini

## Overview
Il comando `docker` è uno strumento fondamentale per gestire container e immagini in un ambiente di virtualizzazione. Permette di creare, eseguire e gestire applicazioni in modo isolato, semplificando il processo di sviluppo e distribuzione.

## Usage
La sintassi di base del comando `docker` è la seguente:

```bash
docker [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni utilizzate con il comando `docker`:

- `run`: Esegue un nuovo container.
- `ps`: Elenca i container in esecuzione.
- `images`: Mostra le immagini disponibili localmente.
- `pull`: Scarica un'immagine da un registro.
- `build`: Costruisce un'immagine a partire da un Dockerfile.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `docker`:

1. **Eseguire un nuovo container**:
   ```bash
   docker run hello-world
   ```
   Questo comando scarica l'immagine `hello-world` e la esegue, mostrando un messaggio di benvenuto.

2. **Elencare i container in esecuzione**:
   ```bash
   docker ps
   ```
   Mostra tutti i container attualmente in esecuzione.

3. **Elencare tutte le immagini disponibili**:
   ```bash
   docker images
   ```
   Visualizza tutte le immagini scaricate e disponibili localmente.

4. **Scaricare un'immagine da un registro**:
   ```bash
   docker pull ubuntu
   ```
   Scarica l'immagine di Ubuntu dal Docker Hub.

5. **Costruire un'immagine da un Dockerfile**:
   ```bash
   docker build -t my-image .
   ```
   Costruisce un'immagine chiamata `my-image` utilizzando il Dockerfile presente nella directory corrente.

## Tips
- Assicurati di avere Docker installato e in esecuzione prima di utilizzare i comandi.
- Utilizza il comando `docker --help` per ottenere ulteriori informazioni su opzioni e argomenti disponibili.
- Mantieni le tue immagini e container aggiornati per garantire la sicurezza e le prestazioni ottimali.
- Considera l'uso di volumi per gestire dati persistenti tra i container.