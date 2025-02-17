# [Linux] Bash ln használat: Hivatkozások létrehozása fájlokhoz

## Overview
A `ln` parancs a Linux és Unix rendszerekben használt parancs, amely lehetővé teszi fájlok és könyvtárak hivatkozásainak létrehozását. Kétféle hivatkozást hozhatunk létre: kemény hivatkozásokat és szimbolikus hivatkozásokat (más néven symlinkek).

## Usage
A `ln` parancs alapvető szintaxisa a következő:

```bash
ln [opciók] [forrás] [cél]
```

## Common Options
- `-s`: Szimbolikus hivatkozás létrehozása.
- `-f`: Felülírja a meglévő hivatkozásokat.
- `-n`: Ha a cél már létezik, ne kövesse a hivatkozást.
- `-v`: Verbose, azaz részletes kimenet, amely megmutatja, hogy mi történik.

## Common Examples
1. **Kemény hivatkozás létrehozása:**
   ```bash
   ln fájl.txt hivatkozás.txt
   ```
   Ez létrehoz egy kemény hivatkozást `hivatkozás.txt` néven a `fájl.txt` fájlra.

2. **Szimbolikus hivatkozás létrehozása:**
   ```bash
   ln -s fájl.txt hivatkozás.txt
   ```
   Ez létrehoz egy szimbolikus hivatkozást `hivatkozás.txt` néven, amely a `fájl.txt` fájlra mutat.

3. **Szimbolikus hivatkozás létrehozása egy könyvtárra:**
   ```bash
   ln -s /path/to/könyvtár hivatkozás_könyvtár
   ```
   Ez létrehoz egy szimbolikus hivatkozást a megadott könyvtárra.

4. **Meglévő hivatkozás felülírása:**
   ```bash
   ln -sf új_fájl.txt hivatkozás.txt
   ```
   Ez felülírja a `hivatkozás.txt` fájlt az `új_fájl.txt` fájlra mutató hivatkozással.

## Tips
- Mindig ellenőrizd, hogy a hivatkozás neve nem ütközik más fájlokkal a célmappában.
- Használj szimbolikus hivatkozásokat, ha a forrásfájlok különböző fájlrendszerekben találhatók.
- A `-v` opció segíthet a hivatkozások létrehozásának nyomon követésében, különösen, ha több fájlt kezelsz egyszerre.