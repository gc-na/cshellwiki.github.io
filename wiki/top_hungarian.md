# [Linux] Bash top használata: A rendszerfolyamatok valós idejű megjelenítése

## Áttekintés
A `top` parancs egy valós idejű rendszerfigyelő eszköz, amely megjeleníti a futó folyamatokat és azok erőforrás-használatát. Segítségével nyomon követhetjük a CPU, memória és egyéb erőforrások kihasználtságát, valamint az aktív folyamatok teljesítményét.

## Használat
A `top` parancs alapvető szintaxisa a következő:

```bash
top [opciók] [argumentumok]
```

## Gyakori opciók
- `-d <másodperc>`: Beállítja a frissítési időtartamot másodpercben.
- `-u <felhasználónév>`: Csak a megadott felhasználó által indított folyamatokat jeleníti meg.
- `-p <PID>`: Csak a megadott folyamat azonosítóját (PID) figyeli.
- `-b`: Batch mód, amely lehetővé teszi a kimenet fájlba írását.

## Gyakori példák
1. A `top` parancs egyszerű futtatása:
   ```bash
   top
   ```

2. A frissítési időtartam beállítása 5 másodpercre:
   ```bash
   top -d 5
   ```

3. Csak egy adott felhasználó folyamatainak megjelenítése:
   ```bash
   top -u username
   ```

4. Egy adott PID figyelése:
   ```bash
   top -p 1234
   ```

5. A `top` kimenetének fájlba írása batch módban:
   ```bash
   top -b -n 1 > top_output.txt
   ```

## Tippek
- Használja a `h` billentyűt a `top` felületen a súgó megjelenítéséhez, ahol további információkat talál a parancs használatáról.
- A `k` billentyű segítségével leállíthat egy folyamatot a PID megadásával.
- A `M` billentyű megnyomásával rendezheti a folyamatokat memóriahasználat szerint, míg a `P` billentyű a CPU használat szerint rendezi őket.