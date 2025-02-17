# [Linux] Bash screen utilizzo: Gestire sessioni di terminale multiple

## Overview
Il comando `screen` è uno strumento potente per gestire sessioni di terminale multiple in modo da poter eseguire processi in background e riprendere il controllo delle sessioni in qualsiasi momento. È particolarmente utile per gli utenti che lavorano su server remoti o che desiderano mantenere attive le loro sessioni anche dopo la disconnessione.

## Usage
La sintassi di base del comando è la seguente:

```
screen [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `screen`:

- `-S <nome>`: Assegna un nome alla sessione, facilitando la gestione delle sessioni multiple.
- `-d -r`: Disconnette una sessione attiva e la riattacca.
- `-list`: Mostra un elenco delle sessioni di screen attive.
- `-L`: Abilita il logging dell'output della sessione in un file.

## Common Examples

### Creare una nuova sessione
Per avviare una nuova sessione di screen, basta digitare:
```
screen
```

### Assegnare un nome alla sessione
Per avviare una sessione con un nome specifico:
```
screen -S mia_sessione
```

### Elencare le sessioni attive
Per vedere tutte le sessioni di screen attive:
```
screen -list
```

### Riattaccare una sessione
Per riattaccare una sessione esistente:
```
screen -r mia_sessione
```

### Disconnettere e riattaccare
Per disconnettere una sessione attiva e riattaccarla successivamente:
```
screen -d -r mia_sessione
```

### Abilitare il logging
Per avviare una sessione con logging attivo:
```
screen -L
```

## Tips
- Usa nomi significativi per le sessioni per facilitare la gestione.
- Ricorda di disconnettere le sessioni quando non sono più necessarie per liberare risorse.
- Puoi utilizzare le combinazioni di tasti `Ctrl+A` seguito da `D` per disconnettere rapidamente una sessione senza chiuderla.