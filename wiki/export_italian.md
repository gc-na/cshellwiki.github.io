# [Linux] C Shell (csh) export utilizzo: Impostare variabili d'ambiente

## Overview
Il comando `export` in C Shell (csh) viene utilizzato per impostare variabili d'ambiente, rendendole disponibili per i processi figli. Questo è utile per configurare l'ambiente di esecuzione di un programma o script.

## Usage
La sintassi di base del comando `export` è la seguente:

```
export [opzioni] [variabili]
```

## Common Options
- **-n**: Rimuove l'esportazione della variabile, rendendola disponibile solo per la shell corrente.
- **-p**: Mostra tutte le variabili d'ambiente attualmente esportate.

## Common Examples

### Esportare una variabile
Per esportare una variabile chiamata `MY_VAR` con il valore `Hello`:

```csh
set MY_VAR = "Hello"
export MY_VAR
```

### Verificare le variabili esportate
Per visualizzare tutte le variabili d'ambiente attualmente esportate:

```csh
export -p
```

### Rimuovere l'esportazione di una variabile
Per rimuovere l'esportazione della variabile `MY_VAR`:

```csh
export -n MY_VAR
```

### Esportare più variabili
Puoi esportare più variabili in un'unica riga:

```csh
set VAR1 = "Value1"
set VAR2 = "Value2"
export VAR1 VAR2
```

## Tips
- Ricorda che le variabili d'ambiente esportate sono disponibili solo per i processi figli avviati dopo l'esportazione.
- Utilizza `export -p` per controllare le variabili d'ambiente prima di eseguire uno script, per assicurarti che le impostazioni siano corrette.
- È buona pratica utilizzare nomi di variabili in maiuscolo per le variabili d'ambiente, per distinguerle dalle variabili locali.