# [Linux] C Shell (csh) tmux utilizzo: Gestire sessioni terminali multiple

## Overview
Il comando `tmux` è un multiplexer di terminale che consente di gestire più sessioni di terminale all'interno di una singola finestra. È utile per gli utenti che desiderano lavorare su più attività contemporaneamente senza dover aprire più finestre del terminale.

## Usage
La sintassi di base del comando `tmux` è la seguente:

```bash
tmux [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `tmux`:

- `new`: Crea una nuova sessione tmux.
- `attach`: Collega una sessione esistente.
- `list-sessions`: Elenca tutte le sessioni tmux attive.
- `kill-session`: Termina una sessione specificata.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `tmux`:

### Creare una nuova sessione
```bash
tmux new -s nome_sessione
```

### Collegarsi a una sessione esistente
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

## Tips
- Usa `Ctrl+b` seguito da `%` per dividere la finestra in due pannelli verticali.
- Usa `Ctrl+b` seguito da `"` per dividere la finestra in due pannelli orizzontali.
- Ricorda di staccare la sessione con `Ctrl+b` seguito da `d` per continuare a lavorare in background.