# [Linux] Bash nohup használata: Futtatás háttérben

## Áttekintés
A `nohup` (no hang up) parancs lehetővé teszi, hogy egy folyamatot háttérben futtassunk, anélkül, hogy az megszakadna, ha a felhasználó kijelentkezik a rendszerből. Ez különösen hasznos hosszú ideig tartó feladatok esetén, mint például adatbázis-migrációk vagy nagy fájlok másolása.

## Használat
A `nohup` parancs alapvető szintaxisa a következő:

```bash
nohup [opciók] [argumentumok]
```

## Gyakori opciók
- `&` - A parancs háttérben való futtatásához használható.
- `-o [fájl]` - A kimenetet egy megadott fájlba irányítja.
- `-e [fájl]` - A hibaüzeneteket egy megadott fájlba irányítja.

## Gyakori példák
1. **Egyszerű parancs háttérben való futtatása:**
   ```bash
   nohup sleep 300 &
   ```
   Ez a parancs 300 másodpercig alszik, és a felhasználó kijelentkezése után is folytatódik.

2. **Kimenet fájlba irányítása:**
   ```bash
   nohup my_script.sh > output.log &
   ```
   A `my_script.sh` kimenete az `output.log` fájlba kerül, miközben a parancs háttérben fut.

3. **Hibaüzenetek külön fájlba irányítása:**
   ```bash
   nohup my_script.sh > output.log 2> error.log &
   ```
   A standard kimenet az `output.log` fájlba, míg a hibaüzenetek az `error.log` fájlba kerülnek.

## Tippek
- Mindig irányítsd a kimenetet és a hibaüzeneteket fájlokba, hogy később vissza tudj nézni a folyamat eredményeire.
- Használj `jobs` parancsot a háttérben futó folyamatok nyomon követésére.
- A `disown` parancs használatával eltávolíthatod a háttérben futó folyamatot a shellből, így az nem fog megszakadni a shell bezárásakor.