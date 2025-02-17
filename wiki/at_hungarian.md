# [Linux] Bash az at parancsnál: Ütemezett parancsok végrehajtása

## Overview
Az `at` parancs lehetővé teszi, hogy egy adott időpontban ütemezett parancsokat futtassunk a Linux rendszeren. Ez hasznos lehet, ha egy feladatot későbbi időpontban szeretnénk végrehajtani, anélkül, hogy folyamatosan figyelnünk kellene rá.

## Usage
A `at` parancs alapvető szintaxisa a következő:

```bash
at [options] [arguments]
```

## Common Options
- `-f FILE`: A megadott fájlból olvassa be a parancsokat.
- `-m`: E-mailt küld a felhasználónak, ha a parancs végrehajtása befejeződött.
- `-q QUEUE`: A parancsot egy adott ütemezési sorba helyezi.
- `-l`: Listázza az ütemezett feladatokat.
- `-d`: Törli a megadott ütemezett feladatot.

## Common Examples
1. **Egyszerű parancs ütemezése:**
   A következő parancs a `hello.sh` scriptet 15:00-kor futtatja:
   ```bash
   echo "/path/to/hello.sh" | at 15:00
   ```

2. **Parancs ütemezése a jövő hétfőn:**
   A következő parancs egy `backup` scriptet futtat a következő hétfőn 10:00-kor:
   ```bash
   echo "/path/to/backup.sh" | at 10:00 next Monday
   ```

3. **Parancs ütemezése fájlból:**
   Ha van egy `commands.txt` fájlunk, amely tartalmazza a futtatni kívánt parancsokat:
   ```bash
   at -f commands.txt 09:00
   ```

4. **Ütemezett feladatok listázása:**
   Az ütemezett feladatok megtekintéséhez használja a következő parancsot:
   ```bash
   at -l
   ```

5. **Ütemezett feladat törlése:**
   A következő parancs törli a megadott azonosítójú ütemezett feladatot:
   ```bash
   at -d 1
   ```

## Tips
- Mindig ellenőrizze az ütemezett feladatokat az `at -l` paranccsal, hogy megbizonyosodjon arról, hogy a kívánt parancsok valóban ütemezve lettek.
- Használja a `-m` opciót, hogy értesítést kapjon a parancsok végrehajtásáról.
- Ügyeljen arra, hogy a parancsok pontosan legyenek megadva, mivel a `at` nem kér visszaigazolást a parancsok helyességéről.