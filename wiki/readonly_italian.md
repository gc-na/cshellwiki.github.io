# [Linux] Bash readonly uso equivalente: Impedisce la modifica delle variabili

## Overview
Il comando `readonly` in Bash viene utilizzato per dichiarare che una variabile è di sola lettura. Una volta che una variabile è contrassegnata come `readonly`, non può essere modificata o eliminata durante la sessione corrente del terminale.

## Usage
La sintassi di base del comando `readonly` è la seguente:

```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: Mostra tutte le variabili di ambiente che sono attualmente contrassegnate come `readonly`.

## Common Examples

### Esempio 1: Dichiarare una variabile come readonly
```bash
readonly VAR="Hello"
```
In questo esempio, la variabile `VAR` è stata dichiarata come `readonly` e non può essere modificata.

### Esempio 2: Tentativo di modifica di una variabile readonly
```bash
readonly VAR="Hello"
VAR="World"  # Questo genererà un errore
```
Questo comando genererà un errore perché `VAR` è stata dichiarata come `readonly`.

### Esempio 3: Visualizzare variabili readonly
```bash
readonly -p
```
Questo comando mostrerà tutte le variabili che sono attualmente contrassegnate come `readonly`.

## Tips
- Utilizza `readonly` per proteggere variabili importanti che non devono essere modificate accidentalmente.
- Ricorda che le variabili di ambiente possono essere rese `readonly` per evitare conflitti in script complessi.
- Se hai bisogno di modificare una variabile `readonly`, dovrai prima rimuovere il suo stato di sola lettura, ma questo non è possibile direttamente; dovrai creare una nuova variabile.