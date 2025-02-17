# [Linux] Bash fold használata: Szövegek sorba tördelése

## Áttekintés
A `fold` parancs a szöveges fájlok sorainak tördelésére szolgál, lehetővé téve, hogy a hosszú sorokat kisebb, kezelhetőbb részekre bontsuk. Ez különösen hasznos lehet, ha a szöveget olyan környezetben szeretnénk megjeleníteni, ahol a sorok hossza korlátozott.

## Használat
A `fold` parancs alapvető szintaxisa a következő:

```bash
fold [opciók] [argumentumok]
```

## Gyakori opciók
- `-w, --width=N`: Beállítja a sorok maximális szélességét N karakterre.
- `-s, --spaces`: A tördelést a szóhatárok mentén végzi, így nem tör el szavakat.
- `-b, --bytes`: A bemeneti szöveg bájtjait veszi figyelembe a tördelés során.

## Gyakori példák
1. **Alapvető használat**: A `file.txt` fájl sorainak tördelése 80 karakter szélességig.
   ```bash
   fold file.txt
   ```

2. **Maximális szélesség beállítása**: A sorok tördelése 50 karakterre.
   ```bash
   fold -w 50 file.txt
   ```

3. **Szóhatárok mentén történő tördelés**: A szöveg tördelése úgy, hogy ne törje el a szavakat.
   ```bash
   fold -s -w 60 file.txt
   ```

4. **Bájtok figyelembevételével**: A bemeneti szöveg bájtjainak figyelembevételével történő tördelés.
   ```bash
   fold -b -w 40 file.txt
   ```

## Tippek
- Használj `-s` opciót, ha fontos, hogy a szavak ne törjenek el, például címek vagy mondatok esetén.
- Kísérletezz a különböző szélességekkel, hogy megtaláld a legjobban olvasható formátumot a céljaidhoz.
- A `fold` parancsot kombinálhatod más parancsokkal, például a `cat`-tel, hogy több fájl tartalmát egyesítsd és tördeld:
  ```bash
  cat file1.txt file2.txt | fold -w 70
  ```