# [Linux] Bash case uso: Gestire le condizioni in modo semplice

## Overview
Il comando `case` in Bash è utilizzato per eseguire una serie di istruzioni in base al valore di una variabile. È simile all'istruzione `switch` in altri linguaggi di programmazione e consente di semplificare la gestione delle condizioni multiple.

## Usage
La sintassi di base del comando `case` è la seguente:

```bash
case [variabile] in
    [pattern1])
        [comandi1]
        ;;
    [pattern2])
        [comandi2]
        ;;
    *)
        [comandi_default]
        ;;
esac
```

## Common Options
Il comando `case` non ha molte opzioni, ma è importante conoscere i seguenti elementi:

- `in`: indica l'inizio dei pattern da confrontare.
- `;;`: segna la fine di un blocco di comandi per un pattern.
- `*`: rappresenta un pattern di default, utilizzato se nessun altro pattern corrisponde.

## Common Examples

### Esempio 1: Esempio base di case
```bash
read -p "Inserisci un numero da 1 a 3: " numero
case $numero in
    1)
        echo "Hai scelto uno."
        ;;
    2)
        echo "Hai scelto due."
        ;;
    3)
        echo "Hai scelto tre."
        ;;
    *)
        echo "Numero non valido."
        ;;
esac
```

### Esempio 2: Utilizzo con stringhe
```bash
read -p "Inserisci il tuo colore preferito: " colore
case $colore in
    "rosso")
        echo "Hai scelto il rosso."
        ;;
    "blu")
        echo "Hai scelto il blu."
        ;;
    "verde")
        echo "Hai scelto il verde."
        ;;
    *)
        echo "Colore non riconosciuto."
        ;;
esac
```

### Esempio 3: Esempio con più pattern
```bash
read -p "Inserisci un giorno della settimana: " giorno
case $giorno in
    "sabato" | "domenica")
        echo "È il fine settimana!"
        ;;
    "lunedì" | "martedì" | "mercoledì" | "giovedì" | "venerdì")
        echo "È un giorno lavorativo."
        ;;
    *)
        echo "Giorno non valido."
        ;;
esac
```

## Tips
- Utilizza il pattern `*` per gestire i casi non previsti e fornire un messaggio di errore.
- Ricorda di terminare ogni blocco di comandi con `;;` per evitare errori di sintassi.
- I pattern possono includere più valori separati da `|`, rendendo il codice più compatto e leggibile.