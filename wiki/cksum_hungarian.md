# [Linux] Bash cksum használata: Ellenőrzi a fájlok ellenőrző összegét

## Áttekintés
A `cksum` parancs a fájlok ellenőrző összegének (checksum) kiszámítására szolgál, amely egyedi azonosítót biztosít a fájlokhoz. Ez segít a fájlok integritásának ellenőrzésében és a hibák észlelésében.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
cksum [opciók] [argumentumok]
```

## Gyakori Opciók
- `-a, --algorithm`: Meghatározza az ellenőrző összeg algoritmusát.
- `--help`: Megjeleníti a parancs használatával kapcsolatos segítséget.
- `--version`: Megjeleníti a verzióinformációkat.

## Gyakori Példák
1. Egy fájl ellenőrző összegének kiszámítása:
   ```bash
   cksum fájl.txt
   ```

2. Több fájl ellenőrző összegének kiszámítása:
   ```bash
   cksum fájl1.txt fájl2.txt
   ```

3. Az ellenőrző összeg algoritmusának megadása:
   ```bash
   cksum --algorithm crc32 fájl.txt
   ```

## Tippek
- Használja a `cksum` parancsot fájlok integritásának ellenőrzésére fájlok másolása előtt és után.
- A `cksum` kimenete tartalmazza a fájl méretét, az ellenőrző összeget és a fájl nevét, így könnyen nyomon követheti a fájlokat.
- Ha több fájlt ellenőriz, érdemes lehet a kimenetet egy fájlba irányítani a későbbi ellenőrzéshez.