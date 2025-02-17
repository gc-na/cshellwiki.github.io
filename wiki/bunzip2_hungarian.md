# [Linux] Bash bunzip2 használata: Fájlok kicsomagolása BZIP2 formátumból

## Áttekintés
A `bunzip2` parancs a BZIP2 tömörítési formátumban lévő fájlok kicsomagolására szolgál. Ez a parancs a tömörített fájlokat visszaállítja az eredeti, kicsomagolt állapotukba.

## Használat
A `bunzip2` parancs alapvető szintaxisa a következő:

```bash
bunzip2 [opciók] [argumentumok]
```

## Gyakori Opciók
- `-k`: Megőrzi az eredeti tömörített fájlt a kicsomagolás után.
- `-f`: Kényszeríti a kicsomagolást, még akkor is, ha a célfájl már létezik.
- `-v`: Részletes kimenetet ad a kicsomagolás folyamatáról.

## Gyakori Példák
1. **Egyszerű kicsomagolás**:
   A `file.bz2` fájl kicsomagolása:
   ```bash
   bunzip2 file.bz2
   ```

2. **Eredeti fájl megőrzése**:
   A `file.bz2` fájl kicsomagolása, miközben az eredeti fájl megmarad:
   ```bash
   bunzip2 -k file.bz2
   ```

3. **Kényszerített kicsomagolás**:
   A `file.bz2` fájl kicsomagolása, ha a célfájl már létezik:
   ```bash
   bunzip2 -f file.bz2
   ```

4. **Részletes kimenet**:
   A kicsomagolás részletes információinak megjelenítése:
   ```bash
   bunzip2 -v file.bz2
   ```

## Tippek
- Mindig ellenőrizze, hogy van-e elegendő hely a lemezen a kicsomagolt fájl számára.
- Használja a `-k` opciót, ha szeretné megőrizni az eredeti tömörített fájlt, amíg nem biztos abban, hogy a kicsomagolás sikeres volt.
- A `bunzip2` parancsot gyakran használják más parancsokkal együtt, például a `tar`-ral, a tömörített archívumok kezelésére.