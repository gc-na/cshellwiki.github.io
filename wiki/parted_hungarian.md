# [Linux] Bash parted használata: Partíciók kezelése

## Áttekintés
A `parted` parancs egy erőteljes eszköz, amely lehetővé teszi a lemezek és partíciók kezelését Linux rendszereken. Segítségével létrehozhatunk, törölhetünk, módosíthatunk és ellenőrizhetünk partíciókat, így ideális választás a lemezkezelési feladatokhoz.

## Használat
A `parted` parancs alapvető szintaxisa a következő:

```bash
parted [opciók] [argumentumok]
```

## Gyakori opciók
- `-s` vagy `--script`: Csendes mód, amely megakadályozza a kérdések feltevését.
- `-l` vagy `--list`: Listázza az összes elérhető lemezt és partíciót.
- `mkpart`: Új partíció létrehozása.
- `rm`: Partíció törlése.
- `resizepart`: Partíció méretének módosítása.

## Gyakori példák

1. **Lemezek listázása**
   ```bash
   parted -l
   ```

2. **Új partíció létrehozása**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Partíció törlése**
   ```bash
   parted /dev/sda rm 1
   ```

4. **Partíció méretének módosítása**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

## Tippek
- Mindig készítsünk biztonsági másolatot a fontos adatokból, mielőtt partíciókat módosítanánk.
- Használjuk a `-s` opciót, ha automatizált szkriptekben dolgozunk, hogy elkerüljük a felhasználói interakciót.
- Ellenőrizzük a partíciók állapotát a `print` paranccsal, mielőtt bármilyen módosítást végeznénk.