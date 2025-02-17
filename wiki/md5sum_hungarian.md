# [Linux] Bash md5sum használat: Fájlok MD5 ellenőrző összegének generálása

## Áttekintés
Az `md5sum` parancs egy olyan eszköz, amely MD5 hash értékeket generál fájlokhoz. Ez a parancs gyakran használatos fájlok integritásának ellenőrzésére, mivel az MD5 hash egyedi az adott fájl tartalmára.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
md5sum [opciók] [argumentumok]
```

## Gyakori opciók
- `-b`: Bináris fájlok feldolgozása.
- `-c`: Ellenőrzi a megadott fájlok MD5 hash értékeit egy fájl alapján.
- `-t`: Csak a fájlok szöveges tartalmát veszi figyelembe.

## Gyakori példák

1. **MD5 hash generálása egy fájlhoz:**

   ```bash
   md5sum fájl.txt
   ```

2. **MD5 hash generálása több fájlhoz:**

   ```bash
   md5sum fájl1.txt fájl2.txt
   ```

3. **MD5 hash ellenőrzése egy fájl alapján:**

   Először generálj egy hash-t és mentsd el egy fájlba:

   ```bash
   md5sum fájl.txt > hash.txt
   ```

   Ezután ellenőrizd a hash-t:

   ```bash
   md5sum -c hash.txt
   ```

4. **MD5 hash generálása bináris fájlhoz:**

   ```bash
   md5sum -b bin_fajl.bin
   ```

## Tippek
- Mindig ellenőrizd a hash értékeket, ha letöltöttél egy fájlt, hogy biztos legyél benne, hogy nem sérült.
- Használj hash fájlokat a fájlok integritásának rendszeres ellenőrzésére.
- Az `md5sum` nem a legbiztonságosabb hash algoritmus, ha érzékeny adatokat kezelsz, érdemes más algoritmusokat, például SHA-256-ot használni.