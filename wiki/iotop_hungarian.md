# [Linux] Bash iotop használata: Az I/O tevékenység figyelése

## Áttekintés
Az `iotop` egy hasznos parancs, amely lehetővé teszi a felhasználók számára, hogy valós időben figyeljék a folyamatok I/O (bemeneti/kimeneti) tevékenységét a Linux operációs rendszeren. Ez segít azonosítani, hogy mely folyamatok használják a legtöbb lemezforgalmat, így könnyebben diagnosztizálhatók a teljesítményproblémák.

## Használat
Az `iotop` parancs alapvető szintaxisa a következő:

```bash
iotop [opciók] [argumentumok]
```

## Gyakori Opciók
- `-o`, `--only`: Csak azokat a folyamatokat mutatja, amelyek jelenleg I/O-t végeznek.
- `-b`, `--batch`: Batch módban fut, amely lehetővé teszi a kimenet fájlba írását.
- `-d`, `--delay`: Beállítja a frissítési időközt másodpercben (alapértelmezett 1 másodperc).
- `-p`, `--pid`: Csak a megadott PID-ű folyamat I/O tevékenységét mutatja.

## Gyakori Példák
1. Az `iotop` alapértelmezett futtatása:
   ```bash
   iotop
   ```

2. Csak az I/O-t végző folyamatok megjelenítése:
   ```bash
   iotop -o
   ```

3. Batch mód használata 2 másodperces frissítési időközönként:
   ```bash
   iotop -b -d 2
   ```

4. Egy adott PID-ű folyamat I/O tevékenységének figyelése:
   ```bash
   iotop -p 1234
   ```

## Tippek
- Használja az `-o` opciót, ha csak az aktív I/O folyamatokat szeretné látni, így könnyebben azonosíthatja a problémás alkalmazásokat.
- A batch mód különösen hasznos, ha a kimenetet fájlba szeretné irányítani, például:
  ```bash
  iotop -b -d 1 > iotop_output.txt
  ```
- Figyelje a legnagyobb I/O-val rendelkező folyamatokat, hogy optimalizálja a rendszer teljesítményét.