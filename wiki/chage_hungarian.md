# [Linux] Bash chage használata: Jelszó érvényességi idő beállítása

## Overview
A `chage` parancs a felhasználói jelszavak érvényességi idejének kezelésére szolgál a Linux operációs rendszerekben. Ezzel a paranccsal beállíthatjuk, hogy a felhasználóknak mikor kell megváltoztatniuk a jelszavukat, valamint egyéb jelszóval kapcsolatos beállításokat is módosíthatunk.

## Usage
A `chage` parancs alapvető szintaxisa a következő:

```bash
chage [opciók] [argumentumok]
```

## Common Options
- `-l, --list`: Megjeleníti a felhasználó jelszóval kapcsolatos információit.
- `-m, --mindays`: Beállítja a minimum napok számát, amelynek el kell telnie a jelszó megváltoztatása előtt.
- `-M, --maxdays`: Beállítja a maximum napok számát, amely után a jelszót kötelező megváltoztatni.
- `-I, --inactive`: Beállítja az inaktív napok számát, amely után a fiók inaktívvá válik.
- `-E, --expire`: Beállítja a jelszó lejárati dátumát.

## Common Examples
1. A felhasználó jelszóval kapcsolatos információinak megjelenítése:
   ```bash
   chage -l felhasználónév
   ```

2. A jelszó minimum napok számának beállítása 5 napra:
   ```bash
   chage -m 5 felhasználónév
   ```

3. A jelszó maximum napok számának beállítása 30 napra:
   ```bash
   chage -M 30 felhasználónév
   ```

4. A jelszó lejárati dátumának beállítása 2024. január 1-re:
   ```bash
   chage -E 2024-01-01 felhasználónév
   ```

5. A jelszó inaktív napok számának beállítása 10 napra:
   ```bash
   chage -I 10 felhasználónév
   ```

## Tips
- Mindig ellenőrizd a felhasználói jelszóval kapcsolatos beállításokat a `-l` opcióval, mielőtt módosítanád őket.
- Használj erős jelszavakat, és állítsd be a maximum napok számát, hogy növeld a rendszer biztonságát.
- Rendszeresen frissítsd a jelszavakat, különösen, ha a felhasználók érzékeny adatokat kezelnek.