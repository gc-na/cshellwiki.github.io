# [Linux] Bash comm parancs: Két fájl összehasonlítása

## Áttekintés
A `comm` parancs a Linux és Unix rendszerekben két rendezett fájl összehasonlítására szolgál. A parancs három oszlopban jeleníti meg az eltéréseket: az első oszlop a csak az első fájlban található sorokat, a második oszlop a csak a második fájlban található sorokat, a harmadik oszlop pedig a közös sorokat tartalmazza.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
comm [opciók] [fájl1] [fájl2]
```

## Gyakori opciók
- `-1`: Ne jelenítse meg az első fájlban található sorokat.
- `-2`: Ne jelenítse meg a második fájlban található sorokat.
- `-3`: Ne jelenítse meg a közös sorokat.
- `-i`: Figyelmen kívül hagyja a kis- és nagybetűk közötti különbséget.

## Gyakori példák
1. Két fájl összehasonlítása és az eltérések megjelenítése:
   ```bash
   comm file1.txt file2.txt
   ```

2. Csak a második fájlban található sorok megjelenítése:
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. Közös sorok megjelenítése, az első fájl sorainak elrejtésével:
   ```bash
   comm -1 file1.txt file2.txt
   ```

4. Kis- és nagybetűk figyelmen kívül hagyása:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tippek
- Győződj meg róla, hogy a fájlok rendezettek, különben a `comm` nem fog megfelelően működni.
- Használj `sort` parancsot a fájlok rendezésére, mielőtt a `comm`-ot alkalmaznád:
  ```bash
  sort file1.txt > sorted_file1.txt
  sort file2.txt > sorted_file2.txt
  comm sorted_file1.txt sorted_file2.txt
  ```
- Használj több opciót egyszerre a kívánt eredmény eléréséhez, például:
  ```bash
  comm -12 file1.txt file2.txt
  ```