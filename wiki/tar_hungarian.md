# [Linux] Bash tar használata: Fájlok tömörítése és archiválása

## Áttekintés
A `tar` parancs egy népszerű Unix/Linux parancs, amely lehetővé teszi fájlok és könyvtárak tömörítését és archiválását. A `tar` (tape archive) segítségével egy vagy több fájlt egyetlen fájlba csomagolhatunk, amely megkönnyíti a fájlok tárolását és átvitelét.

## Használat
A `tar` parancs alapvető szintaxisa a következő:

```bash
tar [opciók] [argumentumok]
```

## Gyakori opciók
- `-c`: Új archívum létrehozása.
- `-x`: Archívum kicsomagolása.
- `-f`: Az archívum fájlnevének megadása.
- `-v`: Verbose (részletes) mód, amely megjeleníti a feldolgozott fájlok nevét.
- `-z`: Gzip tömörítés használata.
- `-j`: Bzip2 tömörítés használata.

## Gyakori példák
1. **Archívum létrehozása**:
   Egy könyvtár (pl. `myfolder`) archívum létrehozása `myarchive.tar` néven:
   ```bash
   tar -cvf myarchive.tar myfolder
   ```

2. **Archívum kicsomagolása**:
   Egy archívum (pl. `myarchive.tar`) kicsomagolása:
   ```bash
   tar -xvf myarchive.tar
   ```

3. **Gzip tömörített archívum létrehozása**:
   Egy könyvtár archívumának létrehozása gzip tömörítéssel:
   ```bash
   tar -czvf myarchive.tar.gz myfolder
   ```

4. **Gzip tömörített archívum kicsomagolása**:
   Gzip tömörített archívum kicsomagolása:
   ```bash
   tar -xzvf myarchive.tar.gz
   ```

5. **Bzip2 tömörített archívum létrehozása**:
   Bzip2 tömörítéssel archiválás:
   ```bash
   tar -cjvf myarchive.tar.bz2 myfolder
   ```

## Tippek
- Mindig ellenőrizze az archívum tartalmát a `-t` opcióval, mielőtt kicsomagolja:
  ```bash
  tar -tvf myarchive.tar
  ```
- Használjon `-C` opciót, hogy megadja a célkönyvtárat, ahová az archívumot kicsomagolja:
  ```bash
  tar -xvf myarchive.tar -C /path/to/destination
  ```
- A tömörítési opciók (pl. `-z` vagy `-j`) használata csökkentheti a fájl méretét, de a tömörítési időt is növelheti.