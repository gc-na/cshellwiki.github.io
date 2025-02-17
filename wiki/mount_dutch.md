# [Linux] Bash mount gebruik: Bevestigen van bestandssystemen

## Overzicht
De `mount`-opdracht in Bash wordt gebruikt om bestandssystemen aan te sluiten op een bepaalde locatie in de bestandshierarchie. Dit maakt het mogelijk om toegang te krijgen tot bestanden en mappen op verschillende schijven of partities.

## Gebruik
De basis syntaxis van de `mount`-opdracht is als volgt:

```bash
mount [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-t type`: Specificeert het type bestandssysteem (bijv. ext4, ntfs).
- `-o opties`: Geeft extra opties op, zoals `ro` (alleen-lezen) of `rw` (lezen en schrijven).
- `-a`: Mount alle bestandssystemen die zijn gedefinieerd in `/etc/fstab`.
- `-r`: Mount het bestandssysteem als alleen-lezen.

## Veelvoorkomende Voorbeelden

1. **Mounten van een USB-stick**:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. **Mounten met een specifiek bestandssysteemtype**:
   ```bash
   mount -t ext4 /dev/sda1 /mnt/data
   ```

3. **Mounten met extra opties**:
   ```bash
   mount -o ro /dev/sr0 /mnt/cdrom
   ```

4. **Alle bestandssystemen mounten uit fstab**:
   ```bash
   mount -a
   ```

## Tips
- Zorg ervoor dat je de juiste rechten hebt om een bestandssysteem te mounten; vaak zijn root-rechten vereist.
- Controleer altijd of het bestandssysteem al is gemount om conflicten te voorkomen.
- Vergeet niet om het bestandssysteem te ontkoppelen met `umount` wanneer je klaar bent om gegevensverlies of beschadiging te voorkomen.