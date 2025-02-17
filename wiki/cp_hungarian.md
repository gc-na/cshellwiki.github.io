# [Linux] Bash cp használata: Fájlok másolása

## Áttekintés
A `cp` parancs a Bash környezetben fájlok és könyvtárak másolására szolgál. Lehetővé teszi, hogy egy vagy több fájlt átmásoljunk egy másik helyre, megkönnyítve ezzel az adatkezelést.

## Használat
A `cp` parancs alapvető szintaxisa a következő:

```bash
cp [opciók] [forrás] [cél]
```

## Gyakori opciók
- `-r`: Rekurzív másolás, könyvtárak másolásához.
- `-i`: Interaktív mód, amely megerősítést kér a felhasználótól, ha a célfájl már létezik.
- `-u`: Csak azokat a fájlokat másolja, amelyek frissebbek a célfájloknál, vagy ha a célfájl nem létezik.
- `-v`: Verbose (részletes) mód, amely megjeleníti a másolás folyamatát.

## Gyakori példák

1. **Egyszerű fájl másolás:**
   ```bash
   cp file.txt backup.txt
   ```
   Ez a parancs a `file.txt` fájlt másolja a `backup.txt` néven.

2. **Könyvtár másolása rekurzívan:**
   ```bash
   cp -r myfolder/ backupfolder/
   ```
   Ezzel a paranccsal a `myfolder` könyvtár és annak tartalma a `backupfolder` könyvtárba kerül másolásra.

3. **Fájl másolása megerősítéssel:**
   ```bash
   cp -i file.txt backup.txt
   ```
   Ha a `backup.txt` már létezik, a rendszer megkérdezi, hogy felül szeretnéd-e írni.

4. **Csak újabb fájlok másolása:**
   ```bash
   cp -u file.txt backup.txt
   ```
   Ez a parancs csak akkor másolja a `file.txt` fájlt, ha az újabb, mint a `backup.txt`.

5. **Részletes másolás:**
   ```bash
   cp -v file.txt backup.txt
   ```
   A `-v` opcióval a parancs megmutatja, hogy a `file.txt` fájl másolása folyamatban van.

## Tippek
- Mindig ellenőrizd a célfájl létezését, különösen, ha nem szeretnéd felülírni.
- Használj `-i` opciót, ha nem vagy biztos abban, hogy a célfájl nem létezik.
- A rekurzív másolás előtt győződj meg róla, hogy a célkönyvtár létezik, különben a parancs hibát fog jelezni.