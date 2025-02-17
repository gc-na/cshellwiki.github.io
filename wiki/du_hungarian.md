# [Linux] Bash du használat: Fájlok és könyvtárak méretének megjelenítése

## Áttekintés
A `du` (disk usage) parancs a fájlok és könyvtárak lemezhasználatának megjelenítésére szolgál. Segítségével könnyen nyomon követhetjük, hogy mennyi helyet foglalnak el az egyes fájlok és mappák a fájlrendszerben.

## Használat
A `du` parancs alapvető szintaxisa a következő:

```bash
du [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Emberi olvasható formátumban jeleníti meg a méreteket (pl. KB, MB).
- `-s`: Csak a megadott könyvtár összesített méretét mutatja.
- `-a`: Minden fájl és könyvtár méretét megjeleníti, nem csak a könyvtárakét.
- `-c`: Összesített méretet ad a megadott fájlokhoz vagy könyvtárakhoz.

## Gyakori példák
1. Az aktuális könyvtár méretének megjelenítése:
   ```bash
   du -h
   ```

2. Egy adott könyvtár méretének összesített megjelenítése:
   ```bash
   du -sh /path/to/directory
   ```

3. Minden fájl és könyvtár méretének megjelenítése az aktuális könyvtárban:
   ```bash
   du -ah
   ```

4. A méretek összesítése több könyvtárra:
   ```bash
   du -ch /path/to/dir1 /path/to/dir2
   ```

## Tippek
- Használja a `-h` opciót, hogy könnyebben értelmezhető méreteket kapjon.
- A `-s` opcióval gyorsan megtudhatja, hogy egy könyvtár mennyi helyet foglal el anélkül, hogy a részletekbe menne.
- A `du` parancsot kombinálhatja más parancsokkal, például a `sort`-tal, hogy a legnagyobb méretű fájlokat vagy könyvtárakat listázza:
  ```bash
  du -ah | sort -hr | head -n 10
  ```
- Rendszeresen ellenőrizze a lemezhasználatot, hogy elkerülje a helyhiányt.