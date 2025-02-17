# [Linux] Bash fg Uso equivalente: Riporta un processo in primo piano

## Overview
Il comando `fg` in Bash è utilizzato per riportare un processo in esecuzione in background al primo piano, consentendo all'utente di interagire direttamente con esso. Questo è particolarmente utile quando si desidera riprendere un processo che è stato sospeso o eseguito in background.

## Usage
La sintassi di base del comando `fg` è la seguente:

```bash
fg [opzioni] [argomenti]
```

## Common Options
- **%n**: Specifica il numero del job che si desidera riportare in primo piano. Ad esempio, `%1` riporterà il primo job in background.
- **%stringa**: Riporta il job che corrisponde alla stringa fornita. Ad esempio, `%myjob` riporterà il job che contiene "myjob" nel suo nome.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `fg`:

### Esempio 1: Riportare il primo job in background
Se hai avviato un processo in background e vuoi riportarlo in primo piano, puoi usare:

```bash
fg %1
```

### Esempio 2: Riportare un job specifico usando il nome
Se hai un job chiamato "editor" e vuoi riportarlo in primo piano, puoi usare:

```bash
fg %editor
```

### Esempio 3: Riportare l'ultimo job in background
Per riportare l'ultimo job in background, puoi semplicemente usare:

```bash
fg
```

## Tips
- Assicurati di controllare i job in background usando il comando `jobs` prima di utilizzare `fg`, per sapere quali processi sono disponibili.
- Se un processo non risponde come previsto, potrebbe essere necessario utilizzare `Ctrl + Z` per sospenderlo prima di riportarlo in primo piano con `fg`.
- Ricorda che `fg` funziona solo con i processi avviati dalla stessa shell. Se un processo è stato avviato in un'altra shell, non sarà possibile riportarlo in primo piano.