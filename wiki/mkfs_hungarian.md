# [Linux] Bash mkfs használata: Fájl rendszer létrehozása

## Áttekintés
A `mkfs` parancs (make filesystem) egy Linux parancs, amely lehetővé teszi fájlrendszerek létrehozását különböző tárolóeszközökön, például merevlemezeken vagy USB meghajtókon. Ez a parancs segít a tárolóeszköz formázásában és a fájlok tárolására alkalmas struktúrák létrehozásában.

## Használat
A `mkfs` parancs alapvető szintaxisa a következő:

```bash
mkfs [opciók] [argumentumok]
```

## Gyakori opciók
- `-t` vagy `--type`: Meghatározza a létrehozandó fájlrendszer típusát (pl. ext4, vfat).
- `-L` vagy `--label`: Címkét ad a fájlrendszernek.
- `-n` vagy `--no-mnt`: Megakadályozza a fájlrendszer automatikus csatolását létrehozás után.
- `-V` vagy `--verbose`: Részletes kimenetet ad a folyamat során.

## Gyakori példák
1. **Ext4 fájlrendszer létrehozása**:
   ```bash
   mkfs -t ext4 /dev/sdb1
   ```

2. **FAT32 fájlrendszer létrehozása**:
   ```bash
   mkfs -t vfat /dev/sdc1
   ```

3. **Fájl rendszer címkézése**:
   ```bash
   mkfs -t ext4 -L mylabel /dev/sdb1
   ```

4. **Részletes kimenet használata**:
   ```bash
   mkfs -V -t ext4 /dev/sdb1
   ```

## Tippek
- Mindig ellenőrizd, hogy a megfelelő eszközt választottad ki, mivel a `mkfs` parancs véglegesen törli az adatokat az adott partíción.
- Használj `lsblk` parancsot a tárolóeszközök és azok partícióinak megtekintésére, mielőtt formáznád őket.
- Készíts biztonsági másolatot az adatokról, mielőtt fájlrendszert hozol létre, hogy elkerüld az adatvesztést.