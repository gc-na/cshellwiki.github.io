# [Linux] Bash rmdir használata: Üres könyvtárak törlése

## Áttekintés
A `rmdir` parancs lehetővé teszi üres könyvtárak törlését a fájlrendszerből. Ha a megadott könyvtár nem üres, a parancs nem hajtódik végre, és hibaüzenetet ad.

## Használat
A `rmdir` parancs alapvető szintaxisa a következő:

```bash
rmdir [opciók] [argumentumok]
```

## Gyakori opciók
- `--ignore-fail-on-non-empty`: Figyelmen kívül hagyja a hibát, ha a könyvtár nem üres.
- `--verbose`: Részletes információt ad a törlésről.
- `--help`: Megjeleníti a parancs használatával kapcsolatos információkat.

## Gyakori példák
1. **Üres könyvtár törlése**
   ```bash
   rmdir pelda_konyvtar
   ```

2. **Több üres könyvtár törlése egyszerre**
   ```bash
   rmdir konyvtar1 konyvtar2 konyvtar3
   ```

3. **Részletes információ a törlésről**
   ```bash
   rmdir --verbose pelda_konyvtar
   ```

4. **Hiba figyelmen kívül hagyása, ha a könyvtár nem üres**
   ```bash
   rmdir --ignore-fail-on-non-empty pelda_konyvtar
   ```

## Tippek
- Mindig ellenőrizd, hogy a törölni kívánt könyvtár üres-e, mielőtt a `rmdir` parancsot használnád.
- Használj `ls` parancsot a könyvtár tartalmának megtekintésére a törlés előtt.
- Ha több könyvtárat szeretnél törölni, győződj meg róla, hogy mindegyik üres, különben a parancs nem fog végrehajtódni.