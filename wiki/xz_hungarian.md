# [Linux] Bash xz használata: Fájlok tömörítése és kicsomagolása

## Áttekintés
Az `xz` parancs egy hatékony tömörítő eszköz, amely a fájlok méretének csökkentésére szolgál. Az `xz` formátum kiváló tömörítési arányt kínál, és gyakran használják szoftvercsomagok és adatarchívumok létrehozására.

## Használat
A parancs alapvető szintaxisa a következő:

```
xz [opciók] [argumentumok]
```

## Gyakori opciók
- `-d`, `--decompress`: Kicsomagolja a tömörített fájlt.
- `-k`, `--keep`: Megőrzi az eredeti fájlt a tömörítés után.
- `-f`, `--force`: Kényszeríti a műveletet, még ha a kimeneti fájl már létezik is.
- `-z`, `--compress`: Tömöríti a fájlt (ez az alapértelmezett művelet).
- `-9`: Maximális tömörítési szint, a legjobb arány elérése érdekében.

## Gyakori példák
1. Fájl tömörítése:
   ```bash
   xz fájl.txt
   ```

2. Fájl kicsomagolása:
   ```bash
   xz -d fájl.txt.xz
   ```

3. Eredeti fájl megtartása tömörítés után:
   ```bash
   xz -k fájl.txt
   ```

4. Maximális tömörítési szint használata:
   ```bash
   xz -9 fájl.txt
   ```

## Tippek
- Használj `-k` opciót, ha szeretnéd megőrizni az eredeti fájlt, amíg a tömörítés folyamatban van.
- A `-f` opcióval kényszerítheted a tömörítést, ha a kimeneti fájl már létezik, de légy óvatos, mert ez felülírhatja a meglévő fájlokat.
- Érdemes megfontolni a tömörítési szintet az idő és a fájlméret közötti egyensúly megtalálása érdekében.