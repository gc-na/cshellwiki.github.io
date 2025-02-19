# [Linux] C Shell (csh) dirname Uso equivalente: Estrae il nome della directory da un percorso

## Overview
Il comando `dirname` è utilizzato per estrarre il nome della directory da un percorso di file. Restituisce la parte del percorso che precede l'ultimo separatore di directory, permettendo di ottenere facilmente la directory in cui si trova un file specifico.

## Usage
La sintassi di base del comando è la seguente:

```
dirname [opzioni] [argomenti]
```

## Common Options
- Non ci sono opzioni comuni per il comando `dirname`, in quanto è progettato per essere semplice e diretto. Accetta solo argomenti che rappresentano i percorsi.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `dirname`:

1. Estrazione del nome della directory da un percorso completo:
   ```csh
   dirname /home/utente/documenti/file.txt
   ```
   Output:
   ```
   /home/utente/documenti
   ```

2. Estrazione del nome della directory da un percorso relativo:
   ```csh
   dirname ./immagini/foto.jpg
   ```
   Output:
   ```
   ./immagini
   ```

3. Utilizzo di `dirname` in un comando per ottenere il percorso della directory corrente:
   ```csh
   dirname $(pwd)
   ```
   Output:
   ```
   /home/utente
   ```

## Tips
- Utilizza `dirname` in combinazione con altri comandi per automatizzare la gestione dei file e delle directory.
- Ricorda che `dirname` non modifica il percorso, ma restituisce solo il nome della directory; quindi puoi usarlo in script senza preoccuparti di alterare i dati.
- Se hai bisogno di ottenere il percorso completo della directory corrente, considera di utilizzare `pwd` insieme a `dirname`.