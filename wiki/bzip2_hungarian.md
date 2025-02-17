# [Linux] Bash bzip2 használata: Fájlok tömörítése és kicsomagolása

## Áttekintés
A `bzip2` parancs egy hatékony tömörítő eszköz, amely a fájlok méretének csökkentésére szolgál. A bzip2 algoritmus általában jobb tömörítési arányt kínál, mint a hagyományos gzip, így ideális nagyobb fájlok esetén.

## Használat
A `bzip2` parancs alapvető szintaxisa a következő:

```bash
bzip2 [opciók] [argumentumok]
```

## Gyakori opciók
- `-d`, `--decompress`: A fájlok kicsomagolására szolgál.
- `-k`, `--keep`: Megőrzi az eredeti fájlt a tömörítés során.
- `-f`, `--force`: Kényszeríti a fájlok felülírását, ha már léteznek.
- `-v`, `--verbose`: Részletes kimenetet ad a tömörítési folyamatról.

## Gyakori példák
1. **Fájl tömörítése**:
   ```bash
   bzip2 file.txt
   ```
   Ez a parancs létrehoz egy `file.txt.bz2` fájlt, és törli az eredeti `file.txt` fájlt.

2. **Fájl kicsomagolása**:
   ```bash
   bzip2 -d file.txt.bz2
   ```
   Ezzel a paranccsal a `file.txt.bz2` fájl kicsomagolásra kerül, és az eredeti `file.txt` fájl visszaáll.

3. **Eredeti fájl megőrzése tömörítéskor**:
   ```bash
   bzip2 -k file.txt
   ```
   Ez a parancs tömöríti a `file.txt` fájlt, de az eredeti fájlt megőrzi.

4. **Több fájl tömörítése egyszerre**:
   ```bash
   bzip2 file1.txt file2.txt
   ```
   Ezzel a paranccsal a `file1.txt` és `file2.txt` fájlok is tömörítésre kerülnek.

## Tippek
- Használj `-v` opciót, ha szeretnéd látni a tömörítési folyamat részleteit.
- Nagy fájlok esetén érdemes először ellenőrizni a szabad lemezterületet, hogy elkerüld a problémákat a tömörítés során.
- A `bzip2` fájlok kicsomagolásához használhatod a `bunzip2` parancsot, amely egy alternatív megoldás a `bzip2 -d` helyett.