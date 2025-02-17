# [Linux] Bash head használata: Az első néhány sor megjelenítése

## Áttekintés
A `head` parancs a fájlok elejéről jelenít meg egy meghatározott számú sort. Alapértelmezés szerint az első 10 sort mutatja, ami hasznos lehet a fájlok gyors áttekintéséhez.

## Használat
A `head` parancs alapvető szintaxisa a következő:

```bash
head [opciók] [fájlok]
```

## Gyakori opciók
- `-n [szám]`: Meghatározza, hogy hány sort szeretnénk megjeleníteni a fájl elejéről.
- `-c [bájt]`: Meghatározza, hogy hány bájtot szeretnénk megjeleníteni a fájl elejéről.
- `-q`: Csak a fájlok tartalmát jeleníti meg, a fájlnevek nélkül.
- `-v`: Minden fájl nevét megjeleníti a tartalom előtt.

## Gyakori példák
1. Az első 10 sor megjelenítése egy fájlból:
   ```bash
   head fájl.txt
   ```

2. Az első 5 sor megjelenítése:
   ```bash
   head -n 5 fájl.txt
   ```

3. Az első 20 bájt megjelenítése:
   ```bash
   head -c 20 fájl.txt
   ```

4. Több fájl első 10 sorának megjelenítése:
   ```bash
   head fájl1.txt fájl2.txt
   ```

5. A fájlok neveinek megjelenítése a tartalom előtt:
   ```bash
   head -v fájl1.txt fájl2.txt
   ```

## Tippek
- Használja a `-n` opciót, ha csak egy bizonyos számú sort szeretne megjeleníteni, ezzel csökkentve a kimenetet.
- A `head` parancsot gyakran kombinálják más parancsokkal, például a `cat` vagy a `grep` parancsokkal, hogy a kimenetet szűkítsék.
- Ha nagy fájlokkal dolgozik, a `head` gyors módot kínál a fájlok tartalmának ellenőrzésére anélkül, hogy az egész fájlt meg kellene nyitnia.