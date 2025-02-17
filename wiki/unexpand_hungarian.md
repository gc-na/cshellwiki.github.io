# [Linux] Bash unexpand használata: A szóközök visszaállítása tabulátorokra

## Áttekintés
Az `unexpand` parancs a szövegfájlokban található szóközöket tabulátorokra cseréli. Ez hasznos lehet, ha a fájlok formázása során tabulátorokat szeretnénk használni a szóközök helyett, így könnyebben olvashatóvá téve a kódot vagy a szöveget.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
unexpand [opciók] [argumentumok]
```

## Gyakori opciók
- `-t, --tabs=SIZE`: Meghatározza a tabulátorok méretét. A SIZE értéke lehet egy szám, amely a tabulátorok közötti szóközök számát jelöli.
- `-a, --all`: Minden szóközt tabulátorra cserél, nem csak a megadott méretűeket.
- `-h, --help`: Megjeleníti a parancs használati útmutatóját.

## Gyakori példák
1. Alapvető használat, ahol a szóközöket tabulátorokra cseréljük:
   ```bash
   unexpand file.txt
   ```

2. Tabulátorok méretének megadása:
   ```bash
   unexpand -t 4 file.txt
   ```

3. Minden szóköz cseréje tabulátorra:
   ```bash
   unexpand -a file.txt
   ```

4. Az eredmény kiírása egy új fájlba:
   ```bash
   unexpand file.txt > output.txt
   ```

## Tippek
- Használj `-t` opciót, hogy a tabulátorok méretét a saját igényeidhez igazítsd.
- Ellenőrizd a fájl tartalmát a `cat` vagy `less` parancsokkal, mielőtt és után használod az `unexpand` parancsot, hogy lásd a változásokat.
- Ha több fájlt szeretnél egyszerre feldolgozni, egyszerűen add hozzá a fájlneveket a parancs végéhez.