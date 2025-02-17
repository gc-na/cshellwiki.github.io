# [Linux] Bash colrm használata: Felesleges oszlopok eltávolítása

## Áttekintés
A `colrm` parancs a Bash környezetben lehetővé teszi a szöveges fájlokból vagy bemenetekből felesleges oszlopok eltávolítását. Hasznos lehet, ha csak bizonyos oszlopokat szeretnénk megjeleníteni, például táblázatos adatok esetén.

## Használat
A `colrm` parancs alapvető szintaxisa a következő:

```bash
colrm [kezdő_oszlop] [vég_oszlop]
```

## Gyakori Opciók
- `kezdő_oszlop`: Az oszlop, amelytől kezdve eltávolítja a szöveget.
- `vég_oszlop`: Az oszlop, amelyig eltávolítja a szöveget.

## Gyakori Példák
1. Az első 5 oszlop eltávolítása egy fájlból:
   ```bash
   colrm 1 5 < input.txt > output.txt
   ```

2. Csak a 3. oszloptól kezdve az összes oszlop eltávolítása:
   ```bash
   colrm 3 < input.txt > output.txt
   ```

3. Az 1. és 3. oszlop közötti szöveg eltávolítása:
   ```bash
   colrm 1 3 < input.txt > output.txt
   ```

## Tippek
- Mindig ellenőrizd a bemeneti fájl formátumát, hogy biztos lehess benne, hogy a kívánt oszlopok megfelelően vannak megadva.
- Használj `cat` parancsot a fájlok megtekintésére a `colrm` előtt, hogy lásd, mely oszlopokat szeretnéd eltávolítani.
- A `colrm` parancsot csővezetékkel is kombinálhatod más parancsokkal, mint például `grep` vagy `awk`, hogy még rugalmasabb megoldásokat kapj.