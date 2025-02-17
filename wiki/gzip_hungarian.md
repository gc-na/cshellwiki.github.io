# [Linux] Bash gzip használata: Fájlok tömörítése

## Áttekintés
A `gzip` parancs egy népszerű tömörítő eszköz a fájlok méretének csökkentésére. A GNU zip (gzip) formátumot használja, amely hatékonyan tömöríti a fájlokat, így azok kevesebb helyet foglalnak el a lemezen.

## Használat
A `gzip` parancs alapvető szintaxisa a következő:

```bash
gzip [opciók] [argumentumok]
```

## Gyakori opciók
- `-d` vagy `--decompress`: A tömörített fájlok kicsomagolására szolgál.
- `-k` vagy `--keep`: Megőrzi az eredeti fájlt a tömörítés során.
- `-v` vagy `--verbose`: Részletes információt ad a tömörítési folyamatról.
- `-r` vagy `--recursive`: Rekurzívan tömöríti a megadott könyvtárakat.

## Gyakori példák
1. **Fájl tömörítése**:
   ```bash
   gzip fájl.txt
   ```
   Ez a parancs létrehozza a `fájl.txt.gz` tömörített fájlt, és törli az eredeti `fájl.txt` fájlt.

2. **Fájl kicsomagolása**:
   ```bash
   gzip -d fájl.txt.gz
   ```
   Ezzel a paranccsal a `fájl.txt.gz` fájl visszaáll a `fájl.txt` eredeti állapotába.

3. **Eredeti fájl megőrzése tömörítéskor**:
   ```bash
   gzip -k fájl.txt
   ```
   Ez a parancs tömöríti a `fájl.txt` fájlt, de az eredeti fájl megmarad.

4. **Több fájl tömörítése egyszerre**:
   ```bash
   gzip fájl1.txt fájl2.txt fájl3.txt
   ```
   Ez a parancs mindhárom fájlt tömöríti.

5. **Rekurzív tömörítés egy könyvtárban**:
   ```bash
   gzip -r könyvtár/
   ```
   A parancs a megadott könyvtárban található összes fájlt tömöríti.

## Tippek
- Mindig ellenőrizd a tömörített fájlok integritását a `gunzip -t fájl.gz` paranccsal.
- Használj `-v` opciót a tömörítési folyamat részletes nyomon követéséhez.
- A `gzip` használata előtt érdemes biztonsági másolatot készíteni az eredeti fájlokról, különösen fontos adatok esetén.