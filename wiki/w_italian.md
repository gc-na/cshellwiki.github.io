# [Linux] Bash w: Visualizza gli utenti connessi e le loro attività

## Overview
Il comando `w` in Bash è utilizzato per visualizzare gli utenti attualmente connessi al sistema e le loro attività. Fornisce informazioni dettagliate come l'ora di accesso, il tempo di inattività e il comando attualmente in esecuzione.

## Usage
La sintassi di base del comando `w` è la seguente:

```
w [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `w`:

- `-h`: Nasconde l'intestazione della tabella.
- `-s`: Mostra un output più compatto, senza informazioni dettagliate.
- `-u`: Mostra solo gli utenti che stanno attualmente utilizzando il sistema.

## Common Examples

### Esempio 1: Visualizzare gli utenti connessi
Per visualizzare un elenco degli utenti attualmente connessi e le loro attività, basta eseguire:

```
w
```

### Esempio 2: Output compatto
Se desideri un output più compatto, puoi utilizzare l'opzione `-s`:

```
w -s
```

### Esempio 3: Nascondere l'intestazione
Per visualizzare le informazioni senza l'intestazione della tabella, usa l'opzione `-h`:

```
w -h
```

### Esempio 4: Mostrare solo utenti attivi
Per visualizzare solo gli utenti attivi, puoi utilizzare l'opzione `-u`:

```
w -u
```

## Tips
- Utilizza `w` regolarmente per monitorare l'attività degli utenti sul tuo sistema.
- Combinando `w` con altre utilità come `grep`, puoi filtrare le informazioni per trovare utenti specifici.
- Ricorda che le informazioni mostrate da `w` possono variare a seconda dei permessi dell'utente che esegue il comando.