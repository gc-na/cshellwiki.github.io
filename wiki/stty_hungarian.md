# [Linux] Bash stty használata: A terminál beállításainak kezelése

## Overview
A `stty` parancs a terminál beállításainak módosítására szolgál. Lehetővé teszi a felhasználók számára, hogy konfigurálják a terminál viselkedését, például a karakterek kezelését, a beviteli és kimeneti módokat, valamint a speciális billentyűk funkcióit.

## Usage
A `stty` parancs alapvető szintaxisa a következő:

```bash
stty [options] [arguments]
```

## Common Options
- `-a`: Megjeleníti az összes beállítást.
- `-g`: Kiírja a jelenlegi beállításokat egy formátumban, amely később visszaállítható.
- `-F <device>`: Megadja a terminál eszközfájlját, amelyet módosítani szeretnénk.
- `erase <char>`: Beállítja a törlő karaktert.
- `kill <char>`: Beállítja a kill karaktert, amely a sort törli.

## Common Examples
1. **Jelenlegi beállítások megjelenítése**:
   ```bash
   stty -a
   ```

2. **Törlő karakter beállítása**:
   ```bash
   stty erase ^H
   ```

3. **Kill karakter beállítása**:
   ```bash
   stty kill ^U
   ```

4. **Beállítások mentése és visszaállítása**:
   ```bash
   stty -g > my_stty_settings.txt
   stty $(cat my_stty_settings.txt)
   ```

5. **Speciális eszköz beállítása**:
   ```bash
   stty -F /dev/ttyUSB0 9600
   ```

## Tips
- Mindig ellenőrizd a beállításokat a `stty -a` paranccsal, mielőtt módosítanád őket.
- Használj `stty -g` parancsot a beállítások mentésére, hogy később könnyen visszaállíthasd őket.
- Légy óvatos a törlő és kill karakterek beállításánál, mivel ezek befolyásolják a parancssori bevitelt.