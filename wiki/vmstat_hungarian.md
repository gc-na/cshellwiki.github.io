# [Linux] Bash vmstat használat: Rendszer teljesítmény figyelése

## Áttekintés
A `vmstat` parancs a rendszer teljesítményének figyelésére szolgál, lehetővé téve a felhasználók számára, hogy információkat kapjanak a memóriahasználatról, a folyamatok állapotáról, a lemezműveletekről és a CPU teljesítményéről.

## Használat
A `vmstat` parancs alapvető szintaxisa a következő:

```bash
vmstat [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Összesített memóriahasználat megjelenítése.
- `-m`: Memória statisztikák megjelenítése.
- `-s`: Részletes statisztikák megjelenítése.
- `-n`: Ne jelenjenek meg a régi statisztikák.
- `interval`: Az időköz, amely után a statisztikák frissülnek (másodpercben).

## Gyakori példák
1. Alapvető rendszerinformációk megjelenítése:
   ```bash
   vmstat
   ```

2. Memóriahasználat részletes megjelenítése:
   ```bash
   vmstat -a
   ```

3. Statisztikák megjelenítése 5 másodpercenként:
   ```bash
   vmstat 5
   ```

4. Részletes statisztikák megjelenítése:
   ```bash
   vmstat -s
   ```

## Tippek
- Használja a `vmstat` parancsot a rendszer teljesítményének gyors ellenőrzésére, különösen hibaelhárítás során.
- Kombinálja más parancsokkal, mint például `top` vagy `htop`, a részletesebb elemzés érdekében.
- Figyelje a CPU és memória használatot, hogy azonosítani tudja a potenciális szűk keresztmetszeteket a rendszerben.