# [Linux] Bash groupmod használata: Csoportok módosítása

## Áttekintés
A `groupmod` parancs lehetővé teszi a felhasználói csoportok módosítását a Linux operációs rendszerekben. Ezzel a parancssal megváltoztathatjuk a csoport nevét, az azonosítóját (GID), és más jellemzőit.

## Használat
A `groupmod` parancs alapvető szintaxisa a következő:

```bash
groupmod [opciók] [érvek]
```

## Gyakori opciók
- `-n, --new-name NÉV`: A csoport új nevének megadása.
- `-g, --gid GID`: A csoport új azonosítójának (GID) beállítása.
- `-o`: Lehetővé teszi az azonos GID használatát más csoportokkal.

## Gyakori példák
1. Csoport névének megváltoztatása:
   ```bash
   groupmod -n uj_csoport regi_csoport
   ```

2. Csoport azonosítójának megváltoztatása:
   ```bash
   groupmod -g 1001 csoport_nev
   ```

3. Csoport azonosítójának megváltoztatása, ha az új GID már létezik:
   ```bash
   groupmod -o -g 1001 csoport_nev
   ```

## Tippek
- Mindig ellenőrizd, hogy a megadott új csoportnév vagy GID nem ütközik-e más csoportokkal, hogy elkerüld a hibákat.
- Használj `getent group` parancsot a csoportok listázásához és az aktuális beállítások ellenőrzéséhez.
- A `groupmod` parancs használata előtt érdemes biztonsági másolatot készíteni a csoportfájlokról.