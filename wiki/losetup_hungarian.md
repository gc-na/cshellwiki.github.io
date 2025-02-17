# [Linux] Bash losetup használat: Virtuális lemezképek kezelése

## Overview
A `losetup` parancs lehetővé teszi a virtuális lemezképek (loop device) kezelését a Linux operációs rendszeren. Ezzel a paranccsal lemezképeket (például ISO fájlokat) csatolhatunk a fájlrendszerhez, így azok úgy viselkednek, mint egy valódi lemez.

## Usage
A `losetup` parancs alapvető szintaxisa a következő:

```bash
losetup [options] [arguments]
```

## Common Options
- `-f`: Az első szabad loop device keresése.
- `-a`: Az összes jelenleg csatolt loop device listázása.
- `-d`: A megadott loop device leválasztása.
- `-o OFFSET`: A lemezkép csatolásának eltolása.
- `-s SIZE`: A lemezkép méretének megadása.

## Common Examples
1. **Első szabad loop device keresése és csatolás egy lemezképhez:**
   ```bash
   losetup -f /path/to/image.img
   ```

2. **Loop device leválasztása:**
   ```bash
   losetup -d /dev/loop0
   ```

3. **Összes csatolt loop device listázása:**
   ```bash
   losetup -a
   ```

4. **Lemezkép csatolása eltolással:**
   ```bash
   losetup -o 2048 /dev/loop1 /path/to/image.img
   ```

5. **Lemezkép méretének megadása csatoláskor:**
   ```bash
   losetup -s 1048576 /dev/loop2 /path/to/image.img
   ```

## Tips
- Mindig ellenőrizd, hogy a loop device szabad-e, mielőtt csatolnád.
- Használj `losetup -a` parancsot a csatolt loop device-ok gyors ellenőrzésére.
- A leválasztás előtt győződj meg arról, hogy a loop device-on lévő fájlrendszer nincs használatban, hogy elkerüld az adatvesztést.