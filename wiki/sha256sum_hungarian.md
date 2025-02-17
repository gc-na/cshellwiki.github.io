# [Linux] Bash sha256sum használata: Fájlok SHA-256 hash értékének kiszámítása

## Áttekintés
A `sha256sum` parancs a fájlok SHA-256 hash értékének kiszámítására szolgál. Ez a parancs hasznos lehet fájlok integritásának ellenőrzésére és az adatok biztonságos tárolására.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
sha256sum [opciók] [argumentumok]
```

## Gyakori opciók
- `-b`, `--binary`: Bináris fájlok hash értékének számítása.
- `-c`, `--check`: Ellenőrzi a megadott hash értékeket a fájlokkal.
- `-h`, `--help`: Információt nyújt a parancs használatáról.
- `-o`, `--output`: A hash értékek kimeneti fájlba írása.

## Gyakori példák

### 1. Fájl hash értékének kiszámítása
```bash
sha256sum fájl.txt
```

### 2. Több fájl hash értékének kiszámítása
```bash
sha256sum fájl1.txt fájl2.txt
```

### 3. Hash értékek ellenőrzése
Először generáljunk egy hash fájlt:
```bash
sha256sum fájl.txt > fájl.txt.sha256
```
Ezután ellenőrizzük a hash értéket:
```bash
sha256sum -c fájl.txt.sha256
```

### 4. Hash értékek bináris fájlokhoz
```bash
sha256sum -b bin_fájl.bin
```

## Tippek
- Mindig ellenőrizd a hash értékeket, ha letöltöttél egy fájlt, hogy biztos legyél az integritásában.
- Használj kimeneti fájlokat a hash értékek tárolására, hogy később könnyen ellenőrizhesd őket.
- A `-c` opció használata lehetővé teszi a hash fájlok gyors ellenőrzését, így érdemes ezt alkalmazni, ha több fájlt kezelsz.