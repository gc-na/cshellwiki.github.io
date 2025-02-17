# [Linux] Bash parted utilizzo: Gestire le partizioni del disco

## Overview
Il comando `parted` è uno strumento potente per gestire le partizioni del disco in sistemi Linux. Permette di creare, modificare e cancellare partizioni, oltre a fornire informazioni dettagliate sulle stesse.

## Usage
La sintassi di base del comando `parted` è la seguente:

```bash
parted [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `parted`:

- `-l`, `--list`: Elenca tutte le partizioni disponibili sui dischi.
- `-s`, `--script`: Esegue il comando in modalità silenziosa, senza richiedere conferma.
- `mkpart`: Crea una nuova partizione.
- `rm`: Rimuove una partizione esistente.
- `resizepart`: Ridimensiona una partizione esistente.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `parted`:

1. **Elencare le partizioni**:
   ```bash
   parted -l
   ```

2. **Creare una nuova partizione**:
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Rimuovere una partizione**:
   ```bash
   parted /dev/sda rm 1
   ```

4. **Ridimensionare una partizione**:
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **Impostare un'etichetta per una partizione**:
   ```bash
   parted /dev/sda mklabel gpt
   ```

## Tips
- Assicurati di eseguire il backup dei dati importanti prima di modificare le partizioni.
- Utilizza l'opzione `-s` per eseguire script senza interruzioni.
- Controlla sempre le modifiche con `parted -l` dopo aver eseguito operazioni di partizionamento per confermare che tutto sia andato a buon fine.