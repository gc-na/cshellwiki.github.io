# [Linux] Bash mount brug: Montering af filsystemer

## Oversigt
`mount`-kommandoen bruges til at montere filsystemer i Linux. Det betyder, at du kan tilslutte et filsystem fra en enhed (som en harddisk eller USB-drev) til et bestemt punkt i filsystemhierarkiet, så du kan få adgang til dets indhold.

## Brug
Den grundlæggende syntaks for `mount`-kommandoen er:

```bash
mount [muligheder] [argumenter]
```

## Almindelige muligheder
- `-t type`: Angiver typen af filsystem, der skal monteres (f.eks. ext4, ntfs).
- `-o options`: Angiver specifikke indstillinger for monteringen, såsom `ro` (read-only) eller `rw` (read-write).
- `-a`: Monterer alle filsystemer, der er angivet i `/etc/fstab`.
- `-r`: Monterer filsystemet som skrivebeskyttet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `mount`-kommandoen:

1. **Montere en USB-drev**:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. **Montere et NTFS-filsystem**:
   ```bash
   mount -t ntfs-3g /dev/sdc1 /mnt/ntfs
   ```

3. **Montere et filsystem som skrivebeskyttet**:
   ```bash
   mount -o ro /dev/sda1 /mnt/data
   ```

4. **Montere alle filsystemer fra fstab**:
   ```bash
   mount -a
   ```

## Tips
- Sørg for at oprette monteringspunktet (f.eks. `/mnt/usb`) før du forsøger at montere en enhed.
- Brug `df -h` for at kontrollere, hvilke filsystemer der er monteret og deres brug.
- For at afmontere et filsystem, brug `umount`-kommandoen efterfulgt af monteringspunktet eller enhedsnavnet.