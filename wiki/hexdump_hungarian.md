# [Linux] Bash hexdump használata: Hexadecimális fájlok megjelenítése

## Overview
A `hexdump` parancs egy fájl tartalmát hexadecimális formátumban jeleníti meg. Hasznos eszköz a bináris fájlok elemzésére, lehetővé téve a felhasználók számára, hogy lássák a fájlok nyers byte-jait.

## Usage
A `hexdump` parancs alapvető szintaxisa a következő:

```bash
hexdump [options] [arguments]
```

## Common Options
- `-C`: Kiterjesztett hexdump formátum, amely a hexadecimális byte-okat és az ASCII karaktereket is megjeleníti.
- `-n <bytes>`: Csak az első `<bytes>` byte-ot jeleníti meg a fájlból.
- `-v`: Minden byte-ot megjelenít, beleértve a duplikált byte-okat is.
- `-e <format>`: Egyéni formátumot ad meg a kimenethez.

## Common Examples
- Hexadecimális dump egy fájlról:
  ```bash
  hexdump myfile.bin
  ```

- Kiterjesztett hexdump formátum használata:
  ```bash
  hexdump -C myfile.bin
  ```

- Csak az első 16 byte megjelenítése:
  ```bash
  hexdump -n 16 myfile.bin
  ```

- Minden byte megjelenítése, beleértve a duplikáltakat is:
  ```bash
  hexdump -v myfile.bin
  ```

- Egyéni formátum használata:
  ```bash
  hexdump -e '16/1 "%02x " "\n"' myfile.bin
  ```

## Tips
- Használj `-C` opciót, ha szeretnéd egyszerre látni a hexadecimális és ASCII karaktereket, ez segíthet a fájlok gyorsabb elemzésében.
- A `-n` opcióval korlátozhatod a megjelenített byte-ok számát, ami hasznos lehet nagy fájlok esetén.
- Kísérletezz az `-e` opcióval, hogy testre szabd a kimenetet, és csak a szükséges információkat jelenítsd meg.