# [Linux] Bash 7z használata: Fájlok tömörítése és kicsomagolása

## Áttekintés
A 7z parancs a 7-Zip fájlkezelő program parancssori interfésze, amely lehetővé teszi fájlok tömörítését és kicsomagolását különböző formátumokban. A 7z formátum a legnagyobb tömörítési arányt kínálja, és támogatja a több fájl archívumok kezelését is.

## Használat
A 7z parancs alapvető szintaxisa a következő:

```
7z [opciók] [argumentumok]
```

## Gyakori opciók
- `a`: Fájlok hozzáadása egy archívumhoz.
- `x`: Fájlok kicsomagolása az archívumból.
- `t`: Archívum típusának megadása.
- `l`: Az archívumban található fájlok listázása.
- `d`: Fájlok törlése az archívumból.

## Gyakori példák

1. **Fájl tömörítése**:
   Az alábbi parancs egy `myarchive.7z` nevű archívumot hoz létre, amely tartalmazza a `file1.txt` és `file2.txt` fájlokat.
   ```bash
   7z a myarchive.7z file1.txt file2.txt
   ```

2. **Fájlok kicsomagolása**:
   A következő parancs kicsomagolja a `myarchive.7z` archívumban található fájlokat.
   ```bash
   7z x myarchive.7z
   ```

3. **Archívum tartalmának listázása**:
   Az alábbi parancs megjeleníti a `myarchive.7z` archívumban található fájlok listáját.
   ```bash
   7z l myarchive.7z
   ```

4. **Fájl törlése az archívumból**:
   A következő parancs törli a `file1.txt` fájlt a `myarchive.7z` archívumból.
   ```bash
   7z d myarchive.7z file1.txt
   ```

## Tippek
- Mindig ellenőrizd az archívum tartalmát a kicsomagolás előtt a `l` opcióval, hogy biztos legyél benne, hogy a megfelelő fájlokat kezeled.
- Használj erős jelszót, ha titkosítani szeretnéd az archívumot a `-p` opcióval.
- Tömörítés előtt érdemes a fájlokat rendezni, hogy a hasonló típusú fájlok egy helyen legyenek, ez javíthatja a tömörítési arányt.