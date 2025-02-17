# [Linux] Bash depmod használat: Modul függőségek kezelése

## Overview
A `depmod` parancs a Linux kernel modulok függőségeinek kezelésére szolgál. Ez a parancs létrehozza a modulok közötti kapcsolatokat, és frissíti a modulok listáját, amely segíti a kernel számára a megfelelő modulok betöltését.

## Usage
A `depmod` parancs alapvető szintaxisa a következő:

```bash
depmod [options] [arguments]
```

## Common Options
- `-a`: Automatikusan frissíti a modulok listáját.
- `-n`: Csak a modulok függőségeit mutatja, nem módosít semmit.
- `-F <file>`: Megadja a kernel verziós fájlt, amelyet használni szeretnénk.
- `-r`: Eltávolítja a megadott modulokat a listából.

## Common Examples
1. A modulok automatikus frissítése:
   ```bash
   depmod -a
   ```

2. A modulok függőségeinek megtekintése anélkül, hogy módosítanánk a listát:
   ```bash
   depmod -n
   ```

3. Egy adott kernel verzió függőségeinek megjelenítése:
   ```bash
   depmod -F /boot/System.map-5.4.0-42-generic
   ```

4. Modul eltávolítása a listából:
   ```bash
   depmod -r modul_neve
   ```

## Tips
- Mindig futtassuk a `depmod -a` parancsot, miután új modulokat telepítettünk, hogy biztosítsuk a megfelelő működést.
- Használjuk a `-n` opciót a teszteléshez, mielőtt végrehajtanánk a módosításokat.
- Ellenőrizzük a `/lib/modules/$(uname -r)/modules.dep` fájlt a modulok függőségeinek megértéséhez.