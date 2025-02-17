# [Linux] Bash tac használat: A fájlok visszafelé történő megjelenítése

## Áttekintés
A `tac` parancs egy egyszerű, de hasznos eszköz a Linux parancssorban, amely a megadott fájlok tartalmát visszafelé, soronként jeleníti meg. A név a "cat" parancs fordított változata, ami arra utal, hogy a `tac` a fájlok sorait fordított sorrendben olvassa be.

## Használat
A `tac` parancs alapvető szintaxisa a következő:

```bash
tac [opciók] [fájlok]
```

## Gyakori Opciók
- `-b`, `--before`: A sorok előtt egy üres sort helyez el.
- `-r`, `--regex`: A bemeneti fájlok sorait reguláris kifejezések alapján dolgozza fel.
- `-s`, `--separator`: A sorok elválasztó karakterét határozza meg.

## Gyakori Példák
1. **Fájl tartalmának visszafelé megjelenítése**:
   ```bash
   tac fajl.txt
   ```

2. **Több fájl tartalmának visszafelé megjelenítése**:
   ```bash
   tac fajl1.txt fajl2.txt
   ```

3. **Üres sorok hozzáadása a sorok elé**:
   ```bash
   tac -b fajl.txt
   ```

4. **Sorok visszafelé megjelenítése egy elválasztó karakter használatával**:
   ```bash
   tac -s ',' fajl.csv
   ```

## Tippek
- Használj `tac`-ot a naplófájlok gyors áttekintésére, ha az utolsó bejegyzéseket szeretnéd látni.
- Kombináld a `tac`-ot más parancsokkal, mint például a `grep`, hogy csak a keresett sorokat jelenítsd meg visszafelé.
- Ne felejtsd el, hogy a `tac` nem módosítja a fájlokat, csak a kimenetet alakítja át, így biztonságosan használhatod fájlok megtekintésére.