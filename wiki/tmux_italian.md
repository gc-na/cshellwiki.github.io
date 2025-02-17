# [Linux] Bash tmux utilizzo: Gestire sessioni di terminale multiple

## Overview
Il comando `tmux` è un multiplexer di terminale che consente di gestire più sessioni di terminale all'interno di una singola finestra. È particolarmente utile per gli utenti che desiderano lavorare su più progetti contemporaneamente o per mantenere sessioni attive anche dopo la disconnessione.

## Usage
La sintassi di base del comando `tmux` è la seguente:

```bash
tmux [opzioni] [argomenti]
```

## Common Options
- `new`: Crea una nuova sessione tmux.
- `attach`: Collega una sessione esistente.
- `list-sessions`: Elenca tutte le sessioni tmux attive.
- `kill-session`: Termina una sessione specificata.
- `detach`: Scollega la sessione corrente.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `tmux`:

### Creare una nuova sessione
```bash
tmux new -s nome_sessione
```

### Attaccarsi a una sessione esistente
```bash
tmux attach -t nome_sessione
```

### Elencare tutte le sessioni attive
```bash
tmux list-sessions
```

### Terminare una sessione
```bash
tmux kill-session -t nome_sessione
```

### Scollegarsi dalla sessione corrente
Premere `Ctrl + b`, seguito da `d`.

## Tips
- Utilizza nomi descrittivi per le tue sessioni per facilitare la gestione.
- Familiarizza con le combinazioni di tasti di tmux per migliorare la tua produttività.
- Salva le configurazioni personalizzate nel file `.tmux.conf` per personalizzare il comportamento di tmux secondo le tue esigenze.