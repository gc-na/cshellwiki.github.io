# [Linux] Bash free használat: Memóriahasználat megjelenítése

## Áttekintés
A `free` parancs a rendszer memóriahasználatának megjelenítésére szolgál. Információt nyújt a használt, szabad és cache-elt memóriáról, valamint a swap területről.

## Használat
A `free` parancs alapvető szintaxisa a következő:

```bash
free [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Emberi olvashatóságú formátumban jeleníti meg az adatokat (pl. MB, GB).
- `-m`: Az értékeket megabájtokban mutatja.
- `-g`: Az értékeket gigabájtokban mutatja.
- `-s [másodperc]`: Folyamatos frissítést biztosít a megadott másodperces időközönként.

## Gyakori példák
1. Alap memóriainformáció megjelenítése:
   ```bash
   free
   ```

2. Emberi olvashatóságú formátumban:
   ```bash
   free -h
   ```

3. Megabájtokban történő megjelenítés:
   ```bash
   free -m
   ```

4. Folyamatos frissítés 5 másodpercenként:
   ```bash
   free -s 5
   ```

## Tippek
- Használja a `-h` opciót, hogy könnyebben értelmezhető formátumban lássa a memóriahasználatot.
- A `free` parancs kimenete hasznos lehet a rendszer teljesítményének monitorozásához, különösen ha memóriahiányos problémákkal küzd.
- Kombinálja a `free` parancsot más parancsokkal, mint például a `watch`, hogy folyamatosan nyomon követhesse a memóriahasználatot.