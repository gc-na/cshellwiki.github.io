# [Linux] C Shell (csh) parted Uso: Gestire le partizioni del disco

## Overview
Il comando `parted` è uno strumento potente per gestire le partizioni del disco. Permette di creare, eliminare, ridimensionare e modificare le partizioni su dischi rigidi e dispositivi di archiviazione.

## Usage
La sintassi di base del comando `parted` è la seguente:

```bash
parted [options] [arguments]
```

## Common Options
- `-l`: Elenca tutte le partizioni disponibili.
- `mkpart`: Crea una nuova partizione.
- `rm`: Rimuove una partizione esistente.
- `resizepart`: Ridimensiona una partizione esistente.
- `print`: Mostra la tabella delle partizioni del disco attualmente selezionato.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `parted`:

1. **Elencare le partizioni disponibili:**
   ```bash
   parted -l
   ```

2. **Creare una nuova partizione:**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Rimuovere una partizione esistente:**
   ```bash
   parted /dev/sda rm 1
   ```

4. **Ridimensionare una partizione:**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **Visualizzare la tabella delle partizioni:**
   ```bash
   parted /dev/sda print
   ```

## Tips
- Assicurati di avere i privilegi di amministratore quando utilizzi `parted`, poiché le modifiche alle partizioni possono influenzare il sistema operativo.
- Fai sempre un backup dei dati importanti prima di apportare modifiche alle partizioni.
- Utilizza il comando `print` per verificare la configurazione attuale delle partizioni prima di eseguire modifiche.