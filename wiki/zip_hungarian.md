# [Linux] Bash zip használata: Fájlok tömörítése

## Áttekintés
A `zip` parancs egy tömörítő eszköz, amely lehetővé teszi fájlok és mappák tömörítését egyetlen ZIP fájlba. Ez segít csökkenteni a fájlok méretét, valamint megkönnyíti a fájlok tárolását és megosztását.

## Használat
A `zip` parancs alapvető szintaxisa a következő:

```bash
zip [opciók] [célfájl] [fájlok]
```

## Gyakori Opciók
- `-r`: Rekurzívan tömörít mappákat.
- `-e`: Titkosítja a ZIP fájlt.
- `-9`: Maximális tömörítési szint.
- `-u`: Frissíti a meglévő ZIP fájlt a megadott fájlokkal.

## Gyakori Példák
- **Egyszerű fájl tömörítése:**
  ```bash
  zip myarchive.zip file1.txt file2.txt
  ```
  Ez a parancs létrehoz egy `myarchive.zip` fájlt, amely tartalmazza a `file1.txt` és `file2.txt` fájlokat.

- **Mappa tömörítése rekurzívan:**
  ```bash
  zip -r myfolder.zip myfolder/
  ```
  Ez a parancs rekurzívan tömöríti a `myfolder` mappát és annak tartalmát.

- **Fájlok frissítése egy meglévő ZIP fájlban:**
  ```bash
  zip -u myarchive.zip file3.txt
  ```
  Ez a parancs frissíti a `myarchive.zip` fájlt a `file3.txt` fájl hozzáadásával.

- **Titkosított ZIP fájl létrehozása:**
  ```bash
  zip -e secure.zip secret.txt
  ```
  Ez a parancs létrehoz egy titkosított ZIP fájlt `secure.zip` néven, amely tartalmazza a `secret.txt` fájlt.

## Tippek
- Mindig ellenőrizd a ZIP fájl tartalmát a `zip -l` paranccsal, hogy megbizonyosodj arról, hogy minden szükséges fájl benne van.
- Használj magas tömörítési szintet (`-9`), ha a fájlok mérete kritikus, de tudd, hogy ez több időt vehet igénybe.
- Ha gyakran használsz ZIP fájlokat, érdemes lehet alias-t létrehozni a parancsok gyorsabb használatához.