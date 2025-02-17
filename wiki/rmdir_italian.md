# [Linux] Bash rmdir utilizzo: Rimuove directory vuote

## Overview
Il comando `rmdir` è utilizzato per rimuovere directory vuote nel sistema operativo Linux. Se la directory contiene file o altre directory, il comando non riuscirà e restituirà un errore.

## Usage
La sintassi di base del comando `rmdir` è la seguente:

```bash
rmdir [opzioni] [argomenti]
```

## Common Options
- `-p`: Rimuove la directory specificata e tutte le sue directory genitore vuote.
- `--ignore-fail-on-non-empty`: Ignora gli errori se la directory non è vuota.

## Common Examples

### Rimuovere una directory vuota
Per rimuovere una directory chiamata `esempio`:

```bash
rmdir esempio
```

### Rimuovere una directory e le sue directory genitore vuote
Se vuoi rimuovere una directory chiamata `figlio` e anche la sua directory genitore `genitore` se è vuota:

```bash
rmdir -p genitore/figlio
```

### Ignorare errori per directory non vuote
Se desideri rimuovere una directory senza preoccuparti se non è vuota:

```bash
rmdir --ignore-fail-on-non-empty esempio
```

## Tips
- Assicurati che la directory sia vuota prima di utilizzare `rmdir`, altrimenti il comando non funzionerà.
- Usa l'opzione `-p` con cautela, poiché rimuoverà anche le directory genitore se sono vuote.
- Controlla sempre il contenuto della directory con `ls` prima di rimuoverla per evitare di perdere dati importanti.