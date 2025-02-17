# [Linux] Bash unrar használata: RAR fájlok kicsomagolása

## Overview
Az `unrar` parancs a RAR archívumok kicsomagolására szolgál. Ezzel a paranccsal könnyedén hozzáférhetünk a RAR fájlokban tárolt adatokhoz.

## Usage
A `unrar` parancs alapvető szintaxisa a következő:

```bash
unrar [opciók] [argumentumok]
```

## Common Options
- `x`: Kicsomagolja az archívumot a megadott könyvtárba.
- `e`: Kicsomagolja az archívumot a jelenlegi könyvtárba, de nem tartalmazza a könyvtárstruktúrát.
- `l`: Megjeleníti az archívumban található fájlok listáját.
- `v`: Részletes információkat ad az archívum tartalmáról.
- `p`: Kérheti a jelszót, ha az archívum jelszóval védett.

## Common Examples
1. RAR fájl kicsomagolása a jelenlegi könyvtárba:
   ```bash
   unrar x minta.rar
   ```

2. RAR fájl kicsomagolása egy megadott könyvtárba:
   ```bash
   unrar x minta.rar /path/to/directory/
   ```

3. Az archívumban található fájlok listájának megjelenítése:
   ```bash
   unrar l minta.rar
   ```

4. Jelszóval védett archívum kicsomagolása:
   ```bash
   unrar x -pJelszo minta.rar
   ```

## Tips
- Mindig ellenőrizze, hogy van-e elegendő hely a kicsomagolt fájlok számára a célkönyvtárban.
- Használja a `l` opciót, hogy először megtekinthesse az archívum tartalmát, mielőtt kicsomagolja.
- Ha jelszóval védett archívumot használ, győződjön meg róla, hogy a jelszót helyesen adja meg, különben a kicsomagolás nem fog sikerülni.