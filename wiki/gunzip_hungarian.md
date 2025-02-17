# [Linux] Bash gunzip használata: Fájlok kicsomagolása

## Áttekintés
A `gunzip` parancs a Gzip tömörített fájlok kicsomagolására szolgál. Ez a parancs lehetővé teszi a felhasználók számára, hogy visszaállítsák a tömörített fájlokat az eredeti formájukba.

## Használat
A `gunzip` parancs alapvető szintaxisa a következő:

```bash
gunzip [opciók] [fájlok]
```

## Gyakori opciók
- `-c`: A kicsomagolt fájl tartalmát a standard kimenetre írja ki, anélkül, hogy a fájlt ténylegesen eltávolítaná.
- `-f`: Kényszeríti a fájlok felülírását, ha már léteznek.
- `-k`: Megőrzi az eredeti tömörített fájlt a kicsomagolás után is.
- `-v`: Részletes információt ad a kicsomagolás folyamatáról.

## Gyakori példák
1. **Egyszerű kicsomagolás**:
   ```bash
   gunzip file.txt.gz
   ```
   Ez a parancs kicsomagolja a `file.txt.gz` fájlt, és eltávolítja a tömörített verziót.

2. **Kicsomagolás a tartalom megjelenítésével**:
   ```bash
   gunzip -c file.txt.gz
   ```
   Ezzel a parancssal a kicsomagolt fájl tartalmát a képernyőre írja ki, anélkül, hogy a fájlt eltávolítaná.

3. **Kicsomagolás felülírással**:
   ```bash
   gunzip -f file.txt.gz
   ```
   Ez a parancs kényszeríti a `file.txt` fájl felülírását, ha már létezik.

4. **Kicsomagolás megőrzéssel**:
   ```bash
   gunzip -k file.txt.gz
   ```
   A `-k` opcióval a tömörített fájl megmarad a kicsomagolás után is.

## Tippek
- Mindig ellenőrizd a fájlok méretét a kicsomagolás előtt, hogy biztos legyél benne, hogy elegendő hely áll rendelkezésre.
- Használj `-v` opciót, ha szeretnéd nyomon követni a kicsomagolás folyamatát.
- Ha több fájlt szeretnél kicsomagolni egyszerre, egyszerűen add hozzá a fájlneveket a parancshoz, például: `gunzip file1.gz file2.gz`.