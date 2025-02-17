# [Linux] Bash cd használata: Könyvtárak közötti navigálás

## Áttekintés
A `cd` parancs (change directory) lehetővé teszi a felhasználók számára, hogy navigáljanak a fájlrendszer könyvtárai között. Ezzel a paranccsal könnyedén átválthatunk egyik könyvtárból a másikba.

## Használat
A `cd` parancs alapvető szintaxisa a következő:

```bash
cd [opciók] [argumentumok]
```

## Gyakori Opciók
- `..` - Visszalépés az aktuális könyvtár szülőkönyvtárába.
- `-` - Visszalépés az előző könyvtárba.
- `~` - Az aktuális felhasználó kezdőkönyvtárának elérése.

## Gyakori Példák
1. **Visszalépés a szülőkönyvtárba:**
   ```bash
   cd ..
   ```

2. **Váltás a felhasználó kezdőkönyvtárába:**
   ```bash
   cd ~
   ```

3. **Váltás egy specifikus könyvtárba:**
   ```bash
   cd /path/to/directory
   ```

4. **Visszalépés az előző könyvtárba:**
   ```bash
   cd -
   ```

## Tippek
- Használj relatív útvonalakat, ha a könyvtárak közel vannak egymáshoz, hogy gyorsabban navigálhass.
- Ellenőrizd az aktuális könyvtárat a `pwd` (print working directory) paranccsal, ha nem vagy biztos a helyzetedben.
- Használj tab-bővítést a könyvtárnevek gyorsabb beírásához.