# [Linux] Bash top utilizzo: visualizzare i processi in tempo reale

## Overview
Il comando `top` è uno strumento di monitoraggio dei processi in tempo reale su sistemi Unix e Linux. Mostra una lista dinamica dei processi in esecuzione, fornendo informazioni dettagliate sull'utilizzo della CPU, della memoria e di altre risorse di sistema.

## Usage
La sintassi di base del comando `top` è la seguente:

```bash
top [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `top`:

- `-d <seconds>`: Imposta il tempo di aggiornamento automatico in secondi.
- `-p <pid>`: Mostra solo il processo con l'ID specificato.
- `-u <user>`: Filtra i processi per un utente specifico.
- `-n <number>`: Esegue il comando per un numero specificato di aggiornamenti e poi termina.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `top`:

1. **Avviare top senza opzioni**:
   ```bash
   top
   ```

2. **Aggiornare ogni 2 secondi**:
   ```bash
   top -d 2
   ```

3. **Mostrare solo un processo specifico**:
   ```bash
   top -p 1234
   ```

4. **Filtrare per utente specifico**:
   ```bash
   top -u username
   ```

5. **Eseguire top per 5 aggiornamenti e poi uscire**:
   ```bash
   top -n 5
   ```

## Tips
- Puoi premere `h` mentre sei in `top` per visualizzare un aiuto interattivo con tutte le scorciatoie da tastiera disponibili.
- Per ordinare i processi in base all'utilizzo della CPU, puoi premere `Shift + P`.
- Per ordinare i processi in base all'utilizzo della memoria, puoi premere `Shift + M`.
- Ricorda che puoi uscire da `top` premendo `q`.