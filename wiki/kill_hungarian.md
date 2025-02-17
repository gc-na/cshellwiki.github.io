# [Linux] Bash kill használata: A folyamatok leállítása

## Overview
A `kill` parancs a Linux és Unix-alapú operációs rendszerekben arra szolgál, hogy jeleket küldjön folyamatoknak. A leggyakoribb használati módja a folyamatok leállítása, de más jelek is küldhetők, amelyek különböző műveleteket hajtanak végre.

## Usage
A `kill` parancs alapvető szintaxisa a következő:

```bash
kill [options] [arguments]
```

## Common Options
- `-l`: Listázza az összes elérhető jel nevét.
- `-s SIGNAL`: Meghatározza a küldendő jelet, ahol a SIGNAL a jel neve vagy száma.
- `-n`: A jel számát adja meg.
- `-p`: Csak a folyamat azonosítóját várja el, nem küld jelet.

## Common Examples
1. **Folyamat leállítása PID alapján**:
   ```bash
   kill 1234
   ```
   (Itt a 1234 a leállítani kívánt folyamat azonosítója.)

2. **Folyamat leállítása SIGTERM jel küldésével**:
   ```bash
   kill -s SIGTERM 1234
   ```

3. **Folyamat leállítása SIGKILL jel küldésével (kényszerített leállítás)**:
   ```bash
   kill -9 1234
   ```

4. **Összes folyamat leállítása egy adott felhasználó által indított folyamatok közül**:
   ```bash
   kill -u username
   ```

5. **Jelek listázása**:
   ```bash
   kill -l
   ```

## Tips
- Mindig ellenőrizd a folyamat azonosítóját (PID) a `ps` vagy `top` parancs segítségével, mielőtt leállítanád.
- Használj kényszerített leállítást (SIGKILL) csak akkor, ha a normál leállítás nem működik, mivel ez nem engedi meg a folyamatnak, hogy tisztán zárja be a működését.
- A `killall` parancs használatával egyszerre több folyamatot is leállíthatsz a nevük alapján.