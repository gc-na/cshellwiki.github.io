# [Linux] Bash vgcreate használata: Létrehoz egy új kötetcsoportot

## Áttekintés
A `vgcreate` parancs a Logical Volume Manager (LVM) eszközkészlet része, amely lehetővé teszi új kötetcsoportok létrehozását a rendszerben. A kötetcsoportok logikai kötetek kezelésére szolgálnak, amelyek rugalmasabbá teszik a tárolóhely kezelését.

## Használat
A `vgcreate` parancs alapvető szintaxisa a következő:

```bash
vgcreate [opciók] [kötetcsoport neve] [fizikai kötetek...]
```

## Gyakori opciók
- `-s, --stripes <szám>`: Beállítja a kötetcsoportra vonatkozó sávok számát.
- `-l, --maxlogicalextents <szám>`: Meghatározza a maximális logikai kiterjedések számát.
- `-n, --nosync`: Az új kötetcsoportot szinkronizálás nélkül hozza létre.
- `-f, --force`: Kényszeríti a kötetcsoport létrehozását, még ha az már létezik is.

## Gyakori példák
1. **Alap kötetcsoport létrehozása**:
   ```bash
   vgcreate my_volume_group /dev/sda1 /dev/sdb1
   ```

2. **Kötetcsoport létrehozása sávokkal**:
   ```bash
   vgcreate -s 64k my_striped_vg /dev/sda1 /dev/sdb1
   ```

3. **Kötetcsoport létrehozása maximális logikai kiterjedésekkel**:
   ```bash
   vgcreate -l 100 my_limited_vg /dev/sda1
   ```

4. **Kötetcsoport létrehozása kényszerítéssel**:
   ```bash
   vgcreate -f my_force_vg /dev/sda1
   ```

## Tippek
- Mindig ellenőrizd, hogy a megadott fizikai kötetek szabadok legyenek, mielőtt létrehozod a kötetcsoportot.
- Használj egyedi és érthető neveket a kötetcsoportok számára, hogy később könnyen azonosíthatóak legyenek.
- Rendszeresen készíts biztonsági másolatot a fontos adatokról, mielőtt módosítanád a kötetcsoportokat.