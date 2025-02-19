# [Linux] C Shell (csh) who uso: Mostra gli utenti connessi

## Overview
Il comando `who` in C Shell (csh) è utilizzato per visualizzare gli utenti attualmente connessi al sistema. Fornisce informazioni come il nome utente, il terminale utilizzato, la data e l'ora di accesso.

## Usage
La sintassi di base del comando `who` è la seguente:

```
who [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `who`:

- `-b`: Mostra l'ultima volta che il sistema è stato avviato.
- `-q`: Mostra solo i nomi degli utenti connessi e il conteggio totale.
- `-H`: Mostra l'intestazione delle colonne.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `who`:

1. Visualizzare tutti gli utenti connessi:
    ```bash
    who
    ```

2. Visualizzare l'ultima volta che il sistema è stato avviato:
    ```bash
    who -b
    ```

3. Mostrare solo i nomi degli utenti connessi e il conteggio totale:
    ```bash
    who -q
    ```

4. Visualizzare gli utenti con un'intestazione delle colonne:
    ```bash
    who -H
    ```

## Tips
- Utilizza `who` regolarmente per monitorare l'attività degli utenti sul tuo sistema.
- Combina `who` con altri comandi come `grep` per filtrare risultati specifici.
- Ricorda che le informazioni mostrate da `who` possono variare a seconda dei permessi dell'utente che esegue il comando.