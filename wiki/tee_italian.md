# [Linux] Bash tee utilizzo: Scrivere in più file contemporaneamente

## Overview
Il comando `tee` in Bash è utilizzato per leggere dall'input standard e scrivere simultaneamente l'output su uno o più file, oltre a visualizzarlo sullo schermo. Questo è particolarmente utile quando si desidera salvare l'output di un comando mentre lo si visualizza.

## Usage
La sintassi di base del comando `tee` è la seguente:

```bash
tee [options] [arguments]
```

## Common Options
- `-a`, `--append`: Aggiunge l'output al file esistente invece di sovrascriverlo.
- `-i`, `--ignore-interrupts`: Ignora i segnali di interruzione.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `--version`: Mostra la versione del comando `tee`.

## Common Examples

### Esempio 1: Scrivere l'output in un file
Per scrivere l'output di un comando in un file, puoi utilizzare:

```bash
echo "Ciao, mondo!" | tee output.txt
```

### Esempio 2: Aggiungere l'output a un file esistente
Se desideri aggiungere l'output a un file già esistente, usa l'opzione `-a`:

```bash
echo "Un'altra riga" | tee -a output.txt
```

### Esempio 3: Scrivere in più file
Puoi anche scrivere l'output in più file contemporaneamente:

```bash
echo "Scrittura in più file" | tee file1.txt file2.txt
```

### Esempio 4: Combinare con altri comandi
`tee` può essere utilizzato in combinazione con altri comandi. Ad esempio, per visualizzare l'output di `ls` e salvarlo in un file:

```bash
ls -l | tee directory_list.txt
```

## Tips
- Utilizza l'opzione `-a` se desideri mantenere il contenuto esistente di un file e aggiungere nuove informazioni.
- Ricorda che `tee` scrive l'output in ordine, quindi l'output visualizzato sullo schermo sarà lo stesso di quello scritto nei file.
- È utile per il debug, poiché puoi monitorare l'output di un comando mentre lo registri in un file per un'analisi successiva.