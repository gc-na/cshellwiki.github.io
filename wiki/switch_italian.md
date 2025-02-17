# [Linux] Bash switch utilizzo: [cambia il comportamento del comando]

## Overview
Il comando `switch` in Bash è utilizzato per gestire il flusso di esecuzione di uno script, permettendo di eseguire diverse azioni in base al valore di una variabile. È simile al comando `case` e offre una struttura chiara per il controllo delle condizioni.

## Usage
La sintassi di base del comando `switch` è la seguente:

```bash
switch [opzioni] [argomenti]
```

## Common Options
- `-e`: specifica un'azione da eseguire in caso di errore.
- `-d`: imposta un valore predefinito se nessun caso corrisponde.
- `-h`: mostra l'aiuto e le opzioni disponibili.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `switch`:

### Esempio 1: Switch semplice
```bash
variabile="cane"

switch $variabile in
    "cane")
        echo "Hai scelto un cane."
        ;;
    "gatto")
        echo "Hai scelto un gatto."
        ;;
    *)
        echo "Scelta non valida."
        ;;
esac
```

### Esempio 2: Switch con valore predefinito
```bash
variabile="uccello"

switch $variabile in
    "cane")
        echo "Hai scelto un cane."
        ;;
    "gatto")
        echo "Hai scelto un gatto."
        ;;
    *)
        echo "Scelta non valida, scegli tra cane o gatto."
        ;;
esac
```

### Esempio 3: Switch con più casi
```bash
giorno="Lunedì"

switch $giorno in
    "Lunedì" | "Martedì" | "Mercoledì")
        echo "Inizio della settimana."
        ;;
    "Giovedì" | "Venerdì")
        echo "Fine della settimana lavorativa."
        ;;
    "Sabato" | "Domenica")
        echo "Weekend!"
        ;;
    *)
        echo "Giorno non valido."
        ;;
esac
```

## Tips
- Utilizza il comando `switch` per migliorare la leggibilità del tuo codice, specialmente quando hai molte condizioni da gestire.
- Assicurati di terminare ogni caso con `;;` per evitare errori di sintassi.
- Ricorda di utilizzare il carattere jolly `*` per gestire i casi non previsti.