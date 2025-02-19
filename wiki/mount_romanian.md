# [Linux] C Shell (csh) mount utilizare: Montarea sistemelor de fișiere

## Overview
Comanda `mount` este utilizată pentru a monta sisteme de fișiere în Linux. Aceasta permite utilizatorilor să acceseze și să utilizeze fișierele de pe dispozitive externe sau de pe alte partiții ale sistemului.

## Usage
Sintaxa de bază a comenzii `mount` este următoarea:
```
mount [opțiuni] [argumente]
```

## Common Options
- `-t type`: Specifică tipul sistemului de fișiere (de exemplu, ext4, ntfs).
- `-o options`: Permite specificarea unor opțiuni suplimentare, cum ar fi `ro` (read-only) sau `rw` (read-write).
- `-a`: Montează toate sistemele de fișiere specificate în `/etc/fstab`.
- `-r`: Montează sistemul de fișiere în mod read-only.

## Common Examples
1. Montarea unei partiții ext4:
   ```bash
   mount -t ext4 /dev/sda1 /mnt
   ```

2. Montarea unui sistem de fișiere NTFS:
   ```bash
   mount -t ntfs-3g /dev/sdb1 /mnt/usb
   ```

3. Montarea tuturor sistemelor de fișiere definite în `/etc/fstab`:
   ```bash
   mount -a
   ```

4. Montarea unei partiții în mod read-only:
   ```bash
   mount -o ro /dev/sda2 /mnt/readonly
   ```

## Tips
- Asigurați-vă că aveți permisiuni suficiente pentru a monta dispozitivele.
- Verificați întotdeauna dacă sistemul de fișiere este curat înainte de a-l monta, folosind comanda `fsck`.
- Utilizați opțiunea `-o uid=USER_ID,gid=GROUP_ID` pentru a seta proprietățile fișierelor montate.