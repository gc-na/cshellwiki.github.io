# [Linux] Bash pidstat használata: Folyamatok statisztikáinak megjelenítése

## Áttekintés
A `pidstat` parancs a Linux operációs rendszerben lehetővé teszi a folyamatok statisztikáinak megjelenítését, például a CPU és memóriahasználatot. Hasznos eszköz a rendszer teljesítményének monitorozásához és a folyamatok viselkedésének elemzéséhez.

## Használat
A `pidstat` parancs alapvető szintaxisa a következő:

```bash
pidstat [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Megjeleníti a segítséget és a parancs használatát.
- `-p <PID>`: Csak a megadott PID-hez tartozó folyamat statisztikáit mutatja.
- `-r`: A memóriahasználati statisztikákat is megjeleníti.
- `-u`: A CPU használati statisztikákat jeleníti meg.
- `-t`: A szálak statisztikáit is megjeleníti.

## Gyakori példák
1. **Alapvető folyamat statisztikák megjelenítése:**
   ```bash
   pidstat
   ```

2. **Csak egy adott PID statisztikáinak megjelenítése:**
   ```bash
   pidstat -p 1234
   ```

3. **CPU és memóriahasználat megjelenítése:**
   ```bash
   pidstat -r -u
   ```

4. **Folyamatok statisztikáinak megjelenítése 1 másodperces intervallummal:**
   ```bash
   pidstat 1
   ```

5. **Szálak statisztikáinak megjelenítése:**
   ```bash
   pidstat -t
   ```

## Tippek
- Használja a `-h` opciót, ha nem biztos a parancs használatában, hogy megismerje a lehetőségeket.
- A `pidstat` kimenete folyamatosan frissíthető, így érdemes egy rövid időintervallumot megadni a folyamatos monitorozáshoz.
- Kombinálja a `pidstat` parancsot más parancsokkal, mint például a `grep`, hogy szűkítse a megjelenített információkat egy adott folyamatra.