# [Linux] Bash fmt használata: Szövegformázás egyszerűen

## Overview
A `fmt` parancs egy egyszerű szövegformázó eszköz, amely a szöveges fájlok sorainak hosszát állítja be, hogy azok esztétikusan és olvashatóan jelenjenek meg. A `fmt` automatikusan tördelheti a szöveget, hogy a sorok ne legyenek túl hosszúak, így a dokumentumok könnyebben olvashatók.

## Usage
A `fmt` parancs alapvető szintaxisa a következő:

```bash
fmt [opciók] [argumentumok]
```

## Common Options
- `-w, --width=N`: Beállítja a sorok maximális hosszát N karakterre.
- `-s, --split-only`: Csak a már meglévő sortöréseket használja, nem tördel újra.
- `-u, --uniform`: Egységesen formázza a szöveget, figyelembe véve a bekezdéseket.

## Common Examples
- Alapértelmezett használat, a szöveg formázása a standard bemenetről:
  ```bash
  fmt < szoveg.txt
  ```

- A sorok maximális hosszának beállítása 50 karakterre:
  ```bash
  fmt -w 50 szoveg.txt
  ```

- Csak a meglévő sortörések használata:
  ```bash
  fmt -s szoveg.txt
  ```

- Egységes formázás bekezdésekkel:
  ```bash
  fmt -u szoveg.txt
  ```

## Tips
- Használj `man fmt` parancsot a `fmt` részletes dokumentációjának megtekintéséhez.
- Kísérletezz különböző opciókkal, hogy megtaláld a legjobban megfelelő formázást a szövegedhez.
- A `fmt` parancsot kombinálhatod más parancsokkal, például a `cat`-tel, hogy több fájlt egyesíts és formázz egyszerre.