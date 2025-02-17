# [Linux] Bash cal <Uso equivalente>: Visualizza un calendario

## Overview
Il comando `cal` in Bash è utilizzato per visualizzare un calendario nel terminale. Mostra il mese corrente o un mese specifico, e può anche visualizzare l'intero anno.

## Usage
La sintassi di base del comando `cal` è la seguente:

```bash
cal [options] [arguments]
```

## Common Options
- `-m`: Mostra il calendario con il lunedì come primo giorno della settimana.
- `-y`: Visualizza l'intero anno.
- `-3`: Mostra il mese corrente, il mese precedente e il mese successivo.
- `-j`: Mostra i giorni dell'anno (numero del giorno) nel calendario.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `cal`:

1. Visualizzare il calendario del mese corrente:
   ```bash
   cal
   ```

2. Visualizzare il calendario di un mese specifico (ad esempio, marzo 2023):
   ```bash
   cal 03 2023
   ```

3. Visualizzare l'intero anno 2023:
   ```bash
   cal -y 2023
   ```

4. Visualizzare il mese corrente con il lunedì come primo giorno della settimana:
   ```bash
   cal -m
   ```

5. Visualizzare il mese corrente, il mese precedente e il mese successivo:
   ```bash
   cal -3
   ```

## Tips
- Utilizza l'opzione `-j` se hai bisogno di riferimenti ai numeri dei giorni dell'anno.
- Puoi combinare le opzioni per personalizzare ulteriormente la visualizzazione del calendario.
- Per una rapida consultazione, puoi utilizzare `cal` senza argomenti per ottenere immediatamente il mese corrente.