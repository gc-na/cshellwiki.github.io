# [Linux] Bash dirname uso: Estrae il percorso della directory

## Overview
Il comando `dirname` in Bash è utilizzato per estrarre il percorso della directory da un percorso di file completo. Questo comando è utile quando si desidera ottenere solo la parte della directory di un percorso, ignorando il nome del file stesso.

## Usage
La sintassi di base del comando è la seguente:

```bash
dirname [opzioni] [argomenti]
```

## Common Options
- `-z`: Tratta gli argomenti come stringhe null terminate.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `--version`: Mostra la versione del comando.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `dirname`:

1. Estrarre la directory da un percorso di file:
   ```bash
   dirname /home/utente/documenti/file.txt
   ```
   Output:
   ```
   /home/utente/documenti
   ```

2. Utilizzare `dirname` con variabili:
   ```bash
   FILE="/home/utente/documenti/file.txt"
   dirname "$FILE"
   ```
   Output:
   ```
   /home/utente/documenti
   ```

3. Estrarre la directory da un percorso relativo:
   ```bash
   dirname ./file.txt
   ```
   Output:
   ```
   .
   ```

4. Utilizzare `dirname` in un ciclo per più file:
   ```bash
   for file in /home/utente/*; do
       echo $(dirname "$file")
   done
   ```
   Output (esempio):
   ```
   /home/utente
   /home/utente
   ```

## Tips
- Utilizza `dirname` in combinazione con altri comandi come `basename` per ottenere sia il percorso della directory che il nome del file.
- Ricorda di racchiudere le variabili tra virgolette per evitare problemi con spazi nei nomi dei file.
- Puoi utilizzare `dirname` in script per automatizzare operazioni sui file e gestire percorsi in modo più efficiente.