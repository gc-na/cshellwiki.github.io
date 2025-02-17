# [Linux] Bash rehash használat: A parancsok újratöltése

## Áttekintés
A `rehash` parancs a Bash környezetben frissíti a parancsok elérhetőségét a parancsértelmező számára. Amikor új parancsokat telepítesz vagy eltávolítasz, a `rehash` segítségével biztosíthatod, hogy a Bash naprakész információkkal rendelkezzen a parancsok helyéről.

## Használat
A `rehash` parancs alapvető szintaxisa a következő:

```bash
rehash [opciók] [argumentumok]
```

## Gyakori opciók
A `rehash` parancsnak nincsenek külön opciói, mivel egyszerűen a parancsok újratöltésére szolgál.

## Gyakori példák
Íme néhány gyakori példa a `rehash` parancs használatára:

1. **Alapértelmezett használat:**
   Frissíti a parancsok elérhetőségét a Bash környezetben.
   ```bash
   rehash
   ```

2. **Új parancs telepítése után:**
   Ha új parancsot telepítettél, futtasd a `rehash`-t, hogy a Bash felismerje azt.
   ```bash
   sudo apt install új-parancs
   rehash
   ```

3. **Parancs eltávolítása után:**
   Ha eltávolítottál egy parancsot, a `rehash` segít frissíteni a parancsok listáját.
   ```bash
   sudo apt remove régi-parancs
   rehash
   ```

## Tippek
- **Használj `rehash`-t gyakran:** Ha gyakran telepítesz vagy távolítasz el parancsokat, érdemes rendszeresen futtatni a `rehash`-t.
- **Ellenőrizd a parancsokat:** A `rehash` futtatása után használhatod a `which` parancsot, hogy ellenőrizd, a Bash megtalálja-e az új parancsokat.
- **Automatizálás:** Beállíthatod a shell indításakor, hogy automatikusan fusson a `rehash`, így mindig naprakész leszel.