# [Linux] C Shell (csh) screen uso equivalente: Gestire sessioni terminale

## Overview
Il comando `screen` è uno strumento potente per gestire sessioni terminali multiple in un'unica finestra. Permette di avviare sessioni di terminale che possono essere staccate e riattaccate, consentendo di continuare a lavorare su processi anche dopo la disconnessione.

## Usage
La sintassi di base del comando `screen` è la seguente:

```csh
screen [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `screen`:

- `-S <nome>`: Assegna un nome alla sessione di screen.
- `-d -r`: Stacca una sessione e la riattacca.
- `-list`: Mostra tutte le sessioni di screen attive.
- `-h <numero>`: Imposta il numero di righe di scrollback.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `screen`:

1. **Avviare una nuova sessione di screen:**
   ```csh
   screen
   ```

2. **Avviare una sessione di screen con un nome specifico:**
   ```csh
   screen -S mia_sessione
   ```

3. **Staccare una sessione di screen:**
   Premere `Ctrl-a` seguito da `d`.

4. **Elencare tutte le sessioni di screen attive:**
   ```csh
   screen -list
   ```

5. **Riattaccare una sessione staccata:**
   ```csh
   screen -r mia_sessione
   ```

## Tips
- Usa nomi significativi per le tue sessioni per facilitarne la gestione.
- Ricorda di staccare le sessioni quando hai finito, per liberare risorse.
- Puoi utilizzare `screen` in combinazione con altri comandi per eseguire script o processi a lungo termine senza dover mantenere il terminale aperto.