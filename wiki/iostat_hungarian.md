# [Linux] Bash iostat használata: Rendszer teljesítményfigyelés

## Áttekintés
Az `iostat` parancs a rendszer teljesítményének figyelésére szolgál, különösen a CPU és a lemez I/O (input/output) statisztikák megjelenítésére. Ezzel a parancssal nyomon követhetjük a rendszer erőforrásainak kihasználtságát, ami segíthet a teljesítményproblémák diagnosztizálásában.

## Használat
A `iostat` parancs alapvető szintaxisa a következő:

```bash
iostat [opciók] [argumentumok]
```

## Gyakori opciók
- `-c`: Csak a CPU statisztikákat jeleníti meg.
- `-d`: Csak a lemez statisztikákat mutatja.
- `-x`: Kiterjesztett statisztikákat ad a lemezekről.
- `-t`: Időbélyeggel ellátott kimenetet generál.
- `interval`: Megadja az időtartamot másodpercben, amely után a statisztikák frissülnek.
- `count`: Megadja, hányszor frissítse a statisztikákat.

## Gyakori példák
1. **Alapvető használat**: Az alap iostat parancs futtatása.
   ```bash
   iostat
   ```

2. **CPU statisztikák megjelenítése**:
   ```bash
   iostat -c
   ```

3. **Díjmentes lemez statisztikák**:
   ```bash
   iostat -d
   ```

4. **Kiterjesztett lemez statisztikák megjelenítése**:
   ```bash
   iostat -x
   ```

5. **Statisztikák frissítése 5 másodpercenként**:
   ```bash
   iostat 5
   ```

6. **Frissítések 5 másodpercenként, 3 alkalommal**:
   ```bash
   iostat 5 3
   ```

## Tippek
- Használja a `-t` opciót, hogy időbélyeggel ellátott statisztikákat kapjon, így könnyebben nyomon követheti a teljesítményváltozásokat.
- Kombinálja az `-x` és `-d` opciókat, ha részletes információra van szüksége a lemezek teljesítményéről.
- Figyelje a CPU kihasználtságot és a lemez I/O-t egyidejűleg, hogy átfogóbb képet kapjon a rendszer állapotáról.