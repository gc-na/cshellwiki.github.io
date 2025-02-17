# [Linux] Bash stat használat: Fájlok és könyvtárak statisztikai információinak megjelenítése

## Áttekintés
A `stat` parancs a fájlok és könyvtárak részletes statisztikai információit jeleníti meg, mint például a fájl mérete, módosítási időpontja és jogosultságai. Hasznos eszköz a fájlok állapotának gyors ellenőrzésére.

## Használat
A `stat` parancs alapvető szintaxisa a következő:

```bash
stat [opciók] [argumentumok]
```

## Gyakori opciók
- `-c` : Egyedi formátumban jeleníti meg az információkat.
- `--format` : Meghatározhatjuk a megjelenítési formátumot.
- `-f` : A fájlrendszer információit mutatja meg.
- `-L` : Követi a szimbolikus linkeket.

## Gyakori példák
1. **Alapvető fájl információk megjelenítése:**
   ```bash
   stat myfile.txt
   ```

2. **Egyedi formátum használata:**
   ```bash
   stat -c '%s bytes' myfile.txt
   ```

3. **Fájl rendszer információk megjelenítése:**
   ```bash
   stat -f myfile.txt
   ```

4. **Szimbolikus linkek követése:**
   ```bash
   stat -L mylink
   ```

## Tippek
- Használj egyedi formátumot a `-c` opcióval, hogy csak a szükséges információkat jelenítsd meg.
- Ellenőrizd a fájlok jogosultságait a `stat` parancs segítségével, hogy biztos lehess benne, hogy a megfelelő hozzáféréssel rendelkezel.
- A `stat` parancsot scripteléshez is használhatod, hogy automatikusan ellenőrizd a fájlok állapotát.