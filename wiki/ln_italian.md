# [Linux] Bash ln utilizzo: Crea collegamenti tra file

## Overview
Il comando `ln` in Bash viene utilizzato per creare collegamenti tra file. Può creare collegamenti "hard" e "symbolic" (o "soft"), consentendo di accedere a file e directory in modi diversi senza duplicare i dati.

## Usage
La sintassi di base del comando `ln` è la seguente:

```bash
ln [opzioni] [argomenti]
```

## Common Options
- `-s`: Crea un collegamento simbolico invece di un collegamento hard.
- `-f`: Forza la creazione del collegamento, sovrascrivendo eventuali file esistenti.
- `-n`: Non seguire i collegamenti simbolici esistenti.
- `-v`: Mostra informazioni dettagliate su ciò che il comando sta facendo.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `ln`:

### Creare un collegamento hard
```bash
ln file_originale.txt collegamento_hard.txt
```

### Creare un collegamento simbolico
```bash
ln -s file_originale.txt collegamento_simbolico.txt
```

### Forzare la creazione di un collegamento
```bash
ln -f file_originale.txt collegamento_hard.txt
```

### Creare un collegamento simbolico a una directory
```bash
ln -s /percorso/directory_originale collegamento_directory
```

## Tips
- Utilizza collegamenti simbolici per riferimenti a file che potrebbero cambiare posizione, poiché i collegamenti hard non possono attraversare i filesystem.
- Controlla sempre i collegamenti creati con `ls -l` per assicurarti che puntino ai file corretti.
- Ricorda che i collegamenti hard non possono essere creati per directory a meno che non si utilizzi `root`.