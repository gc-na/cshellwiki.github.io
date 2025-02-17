# [Linux] Bash wget használata: Fájlok letöltése az internetről

## Áttekintés
A `wget` egy parancssori eszköz, amely lehetővé teszi fájlok letöltését az internetről. Képes HTTP, HTTPS és FTP protokollok használatára, így széleskörű alkalmazási lehetőségeket kínál.

## Használat
A `wget` parancs alapvető szintaxisa a következő:

```bash
wget [opciók] [argumentumok]
```

## Gyakori opciók
- `-O [fájl]`: A letöltött fájl nevét megadhatjuk.
- `-c`: Folytatja a megszakított letöltést.
- `-q`: Csendes mód, nem jelenít meg kimenetet.
- `--limit-rate=[sebesség]`: Korlátozza a letöltési sebességet.
- `-r`: Rekurzív letöltés, mappák és almappák letöltésére.

## Gyakori példák
1. Egyszerű fájl letöltése:
   ```bash
   wget https://example.com/fajl.txt
   ```

2. Fájl letöltése egy megadott névvel:
   ```bash
   wget -O uj_fajl.txt https://example.com/fajl.txt
   ```

3. Megszakított letöltés folytatása:
   ```bash
   wget -c https://example.com/nagy_fajl.zip
   ```

4. Csendes letöltés:
   ```bash
   wget -q https://example.com/fajl.txt
   ```

5. Rekurzív letöltés:
   ```bash
   wget -r https://example.com/mappa/
   ```

## Tippek
- Használj `-c` opciót, ha nagy fájlokat töltesz le, így elkerülheted a letöltés újraindítását.
- A `--limit-rate` opcióval szabályozhatod a sávszélességet, hogy más internetes tevékenységeket ne zavarj.
- Ellenőrizd a letöltési linket, hogy biztos legyél benne, hogy a fájl elérhető és megbízható forrásból származik.