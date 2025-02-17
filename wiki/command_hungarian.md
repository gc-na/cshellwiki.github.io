# [Linux] Bash parancs használata: Fájlok és könyvtárak listázása

## Áttekintés
A `ls` parancs a fájlok és könyvtárak listázására szolgál a Linux és Unix rendszereken. Ez a parancs lehetővé teszi a felhasználók számára, hogy gyorsan áttekintsék a jelenlegi könyvtár tartalmát, és különböző opciókkal testre szabják a megjelenítést.

## Használat
A `ls` parancs alapvető szintaxisa a következő:

```bash
ls [opciók] [könyvtár]
```

## Gyakori opciók
- `-l`: Hosszú formátumú listázás, amely részletes információkat ad a fájlokról (pl. jogosultságok, méret, módosítás dátuma).
- `-a`: Minden fájl megjelenítése, beleértve a rejtett fájlokat is (amelyek neve ponttal kezdődik).
- `-h`: Emberi olvashatóságú méretek (pl. Kb, Mb) megjelenítése.
- `-R`: Rekurzív listázás, amely a megadott könyvtár összes almappáját is megjeleníti.

## Gyakori példák
1. A jelenlegi könyvtár fájljainak listázása:
   ```bash
   ls
   ```

2. A fájlok részletes listázása:
   ```bash
   ls -l
   ```

3. A rejtett fájlok megjelenítése:
   ```bash
   ls -a
   ```

4. A fájlok emberi olvashatóságú méretekkel való listázása:
   ```bash
   ls -lh
   ```

5. Rekurzív listázás egy adott könyvtárban:
   ```bash
   ls -R /path/to/directory
   ```

## Tippek
- Használj több opciót egyszerre a parancsban, például `ls -la` a részletes és rejtett fájlok megjelenítéséhez.
- A `ls` parancs kimenetének rendezéséhez használhatod a `-t` opciót, amely a fájlokat módosítás dátuma szerint rendezi.
- A `--color` opcióval színes kimenetet kaphatsz, amely segít a fájlok gyorsabb azonosításában.