# [Linux] Bash ls használata: fájlok és könyvtárak listázása

## Áttekintés
Az `ls` parancs a fájlok és könyvtárak listázására szolgál a Linux és Unix alapú rendszereken. Segítségével könnyen megtekinthetjük a jelenlegi könyvtár tartalmát, valamint különböző információkat is kaphatunk a fájlokról.

## Használat
A `ls` parancs alapvető szintaxisa a következő:

```bash
ls [opciók] [argumentumok]
```

## Gyakori opciók
- `-l`: Hosszú formátumú listázás, amely részletes információkat ad a fájlokról (pl. jogosultságok, fájlméret, módosítás dátuma).
- `-a`: Minden fájl megjelenítése, beleértve a rejtett fájlokat is (amelyek neve ponttal kezdődik).
- `-h`: Ember által olvasható formátumban jeleníti meg a fájlméreteket (pl. KB, MB).
- `-R`: Rekurzív listázás, amely a könyvtárak tartalmát is megjeleníti, beleértve a belső könyvtárakat is.
- `-t`: A fájlokat a módosítás ideje szerint rendezi, legújabb elöl.

## Gyakori példák
1. Alapértelmezett fájlok listázása:
   ```bash
   ls
   ```

2. Rejtett fájlok megjelenítése:
   ```bash
   ls -a
   ```

3. Hosszú formátumú listázás:
   ```bash
   ls -l
   ```

4. Ember által olvasható fájlméretek:
   ```bash
   ls -lh
   ```

5. Fájlok rendezése módosítás ideje szerint:
   ```bash
   ls -lt
   ```

6. Rekurzív listázás:
   ```bash
   ls -R
   ```

## Tippek
- Használj több opciót egyszerre, például `ls -la` a rejtett fájlok részletes listázásához.
- A `tab` billentyű használata segíthet a fájlnevek automatikus kiegészítésében.
- A `ls` parancs kimenete színes lehet, ha a terminálod támogatja a színes megjelenítést, így könnyebben megkülönböztetheted a fájlokat és könyvtárakat.