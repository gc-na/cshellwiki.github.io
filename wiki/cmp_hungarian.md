# [Linux] Bash cmp használata: Fájlok összehasonlítása

## Áttekintés
A `cmp` parancs a fájlok byte-szintű összehasonlítására szolgál. Segítségével megállapíthatjuk, hogy két fájl azonos-e, és ha nem, akkor hol térnek el egymástól.

## Használat
A `cmp` parancs alapvető szintaxisa a következő:

```bash
cmp [opciók] [fájl1] [fájl2]
```

## Gyakori opciók
- `-l`: Kiírja a különbségeket byte-onként, hexadecimális formátumban.
- `-s`: Csupán jelez, ha a fájlok eltérnek, de nem ír ki részleteket.
- `-i OFFSET`: Az összehasonlítást az OFFSET byte-tól kezdi.
- `--help`: Megjeleníti a parancs használati útmutatóját.

## Gyakori példák
- Két fájl egyszerű összehasonlítása:
    ```bash
    cmp file1.txt file2.txt
    ```

- Különbségek kiírása hexadecimális formátumban:
    ```bash
    cmp -l file1.bin file2.bin
    ```

- Csupán a fájlok eltérésének ellenőrzése:
    ```bash
    cmp -s file1.txt file2.txt
    ```

- Az összehasonlítás kezdése egy adott byte-tól:
    ```bash
    cmp -i 10 file1.txt file2.txt
    ```

## Tippek
- Használj `-s` opciót, ha csak az eltérések meglétét szeretnéd ellenőrizni, anélkül, hogy részleteket írnál ki.
- A `cmp` parancs ideális bináris fájlok összehasonlítására, mivel byte-szinten működik.
- Ha a fájlok eltéréseinek részletes elemzésére van szükséged, érdemes a `diff` parancsot használni, amely szöveges fájlok esetén jobban alkalmazható.