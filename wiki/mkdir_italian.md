# [Linux] C Shell (csh) mkdir Uso: Crea directory nel file system

## Overview
Il comando `mkdir` viene utilizzato per creare nuove directory nel file system. È uno strumento fondamentale per l'organizzazione dei file e delle cartelle.

## Usage
La sintassi di base del comando `mkdir` è la seguente:

```csh
mkdir [opzioni] [argomenti]
```

## Common Options
- `-p`: Crea directory genitore se non esistono già.
- `-m`: Imposta i permessi della directory al valore specificato.
- `-v`: Mostra un messaggio per ogni directory creata.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `mkdir`:

1. Creare una singola directory:
   ```csh
   mkdir nuova_cartella
   ```

2. Creare più directory contemporaneamente:
   ```csh
   mkdir cartella1 cartella2 cartella3
   ```

3. Creare una directory e tutte le directory genitore necessarie:
   ```csh
   mkdir -p /percorso/verso/nueva_cartella
   ```

4. Creare una directory con permessi specifici:
   ```csh
   mkdir -m 755 cartella_pubblica
   ```

5. Creare una directory e visualizzare un messaggio di conferma:
   ```csh
   mkdir -v cartella_di_test
   ```

## Tips
- Utilizza l'opzione `-p` quando non sei sicuro se le directory genitore esistono già, per evitare errori.
- Controlla i permessi delle directory create per garantire che siano appropriati per l'uso previsto.
- Usa l'opzione `-v` per confermare che le directory siano state create correttamente, specialmente quando crei più directory in una sola volta.