# [Linux] Bash col használata: Szövegformázás és szűrés

## Overview
A `col` parancs a szövegformázásra és a szűrésre szolgál, amely eltávolítja a formázási karaktereket a szövegből, és lehetővé teszi a szöveg megfelelő megjelenítését.

## Usage
A `col` parancs alapvető szintaxisa a következő:

```bash
col [opciók] [argumentumok]
```

## Common Options
- `-b`: Eltávolítja a visszafelé irányuló tabulátorokat.
- `-x`: A tabulátorokat a legközelebbi oszlop határához igazítja.
- `-f`: Eltávolítja a formázási karaktereket, például a visszafelé irányuló tabulátorokat.

## Common Examples
1. **Egyszerű szöveg szűrése**:
   A `col` parancs használata egy fájlban található formázási karakterek eltávolítására.
   ```bash
   col < bemenet.txt > kimenet.txt
   ```

2. **Visszafelé irányuló tabulátorok eltávolítása**:
   Ha csak a visszafelé irányuló tabulátorokat szeretnénk eltávolítani.
   ```bash
   col -b < bemenet.txt > kimenet.txt
   ```

3. **Tabulátorok igazítása**:
   A tabulátorok igazítása a legközelebbi oszlop határához.
   ```bash
   col -x < bemenet.txt > kimenet.txt
   ```

## Tips
- Használj `cat -e` parancsot a fájl tartalmának megtekintésére, hogy láthasd a formázási karaktereket, mielőtt a `col` parancsot alkalmaznád.
- A `col` parancsot gyakran használják más parancsokkal együtt, például a `man` parancs kimenetének formázására.
- Győződj meg róla, hogy a bemeneti fájl szövege megfelelően van kódolva, hogy a `col` parancs hatékonyan működjön.