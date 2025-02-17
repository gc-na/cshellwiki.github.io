# [Linux] Bash dpkg használata: Csomagkezelés Debian alapú rendszerekben

## Overview
A `dpkg` parancs a Debian alapú Linux rendszerek csomagkezelője, amely lehetővé teszi a szoftvercsomagok telepítését, eltávolítását és kezelését. A `dpkg` közvetlenül a `.deb` fájlokkal dolgozik, és alapvető eszköz a csomagok kezelésére.

## Usage
A `dpkg` parancs alapvető szintaxisa a következő:

```bash
dpkg [options] [arguments]
```

## Common Options
- `-i`, `--install`: Telepít egy csomagot.
- `-r`, `--remove`: Eltávolít egy csomagot.
- `-l`, `--list`: Megjeleníti a telepített csomagok listáját.
- `-s`, `--status`: Megjeleníti egy csomag állapotát.
- `-c`, `--contents`: Megjeleníti a csomag tartalmát.

## Common Examples
- **Csomag telepítése**:
  ```bash
  sudo dpkg -i csomagneve.deb
  ```

- **Csomag eltávolítása**:
  ```bash
  sudo dpkg -r csomagneve
  ```

- **Telepített csomagok listázása**:
  ```bash
  dpkg -l
  ```

- **Csomag állapotának megtekintése**:
  ```bash
  dpkg -s csomagneve
  ```

- **Csomag tartalmának megtekintése**:
  ```bash
  dpkg -c csomagneve.deb
  ```

## Tips
- Mindig használj `sudo`-t a `dpkg` parancsok előtt, ha rendszerszintű csomagokat kezelsz.
- Ellenőrizd a csomag függőségeit a telepítés előtt, mivel a `dpkg` nem kezeli automatikusan a függőségeket.
- Használj `apt`-ot a `dpkg` helyett, ha a csomagkezelés során automatikus függőségkezelést szeretnél.