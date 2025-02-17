# [Linux] Bash export utilizzo: Imposta variabili d'ambiente

## Overview
Il comando `export` in Bash è utilizzato per impostare variabili d'ambiente, rendendole disponibili per i processi figli. Quando una variabile è esportata, i programmi eseguiti da quella shell possono accedervi.

## Usage
La sintassi di base del comando `export` è la seguente:

```bash
export [options] [arguments]
```

## Common Options
- `-p`: Mostra tutte le variabili d'ambiente attualmente esportate.
- `-n`: Rimuove l'esportazione di una variabile, rendendola non più disponibile per i processi figli.
- `-f`: Esporta una funzione definita nella shell.

## Common Examples

### Esportare una variabile
Per esportare una variabile chiamata `MY_VAR`:

```bash
MY_VAR="Hello, World!"
export MY_VAR
```

### Verificare le variabili esportate
Per visualizzare tutte le variabili d'ambiente esportate:

```bash
export -p
```

### Rimuovere l'esportazione di una variabile
Per rimuovere l'esportazione di `MY_VAR`:

```bash
export -n MY_VAR
```

### Esportare una funzione
Per esportare una funzione chiamata `my_function`:

```bash
my_function() {
    echo "This is my function"
}
export -f my_function
```

## Tips
- Ricorda che le variabili d'ambiente esportate sono visibili solo ai processi figli avviati dopo l'esportazione.
- È buona pratica utilizzare nomi di variabili in maiuscolo per le variabili d'ambiente, per distinguerle dalle variabili locali.
- Puoi combinare l'assegnazione e l'esportazione in un'unica riga: `export MY_VAR="value"`.