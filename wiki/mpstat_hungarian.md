# [Linux] Bash mpstat használata: A CPU statisztikák megjelenítése

## Áttekintés
Az `mpstat` parancs a CPU statisztikák megjelenítésére szolgál, lehetővé téve a felhasználók számára, hogy nyomon követhessék a rendszer teljesítményét és a processzorok terhelését.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
mpstat [opciók] [argumentumok]
```

## Gyakori lehetőségek
- `-P ALL`: Minden CPU statisztikájának megjelenítése.
- `-u`: A CPU kihasználtságának megjelenítése.
- `-r`: A rendszer statisztikáinak megjelenítése.
- `-h`: Az információk emberi olvasásra alkalmas formátumban való megjelenítése.
- `interval`: Az adatok frissítési intervalluma másodpercben.

## Gyakori példák
1. Minden CPU statisztikájának megjelenítése:
   ```bash
   mpstat -P ALL
   ```

2. CPU kihasználtságának megjelenítése 5 másodpercenként:
   ```bash
   mpstat -u 5
   ```

3. Rendszer statisztikáinak megjelenítése:
   ```bash
   mpstat -r
   ```

4. Az adatok megjelenítése emberi olvasásra alkalmas formátumban:
   ```bash
   mpstat -h
   ```

## Tippek
- Használja az `-P ALL` opciót, ha több processzorral rendelkező rendszeren szeretné nyomon követni az egyes CPU-k teljesítményét.
- Az `interval` paraméter használatával folyamatosan figyelheti a CPU statisztikákat, ami segíthet a teljesítményproblémák azonosításában.
- A `mpstat` parancs kimenetét irányíthatja fájlba, hogy később elemezhesse az adatokat:
  ```bash
  mpstat -P ALL 5 > cpu_stats.txt
  ```