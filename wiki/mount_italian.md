# [Linux] Bash mount utilizzo: Montare file system

## Overview
Il comando `mount` in Bash è utilizzato per montare file system su directory specifiche nel sistema operativo. Permette di accedere a dispositivi di archiviazione come hard disk, chiavette USB e partizioni, rendendo i loro contenuti disponibili per l'uso.

## Usage
La sintassi di base del comando `mount` è la seguente:

```bash
mount [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `mount`:

- `-t tipo`: Specifica il tipo di file system da montare (es. `ext4`, `ntfs`).
- `-o options`: Permette di specificare opzioni di montaggio come `ro` (read-only) o `rw` (read-write).
- `-a`: Monta tutti i file system elencati in `/etc/fstab`.
- `-r`: Monta il file system in modalità sola lettura.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `mount`:

1. **Montare una chiavetta USB**:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. **Montare un file system NTFS in modalità lettura e scrittura**:
   ```bash
   mount -t ntfs-3g -o rw /dev/sdc1 /mnt/ntfs
   ```

3. **Montare un file system ext4 in modalità sola lettura**:
   ```bash
   mount -t ext4 -o ro /dev/sda1 /mnt/ext4
   ```

4. **Montare tutti i file system definiti in fstab**:
   ```bash
   mount -a
   ```

## Tips
- Assicurati di avere i permessi necessari per montare dispositivi; potresti dover usare `sudo`.
- Controlla sempre il punto di montaggio per evitare conflitti con altre directory.
- Usa il comando `umount` per smontare i file system quando non sono più necessari.