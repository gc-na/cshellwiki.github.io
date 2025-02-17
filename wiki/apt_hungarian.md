# [Linux] Bash apt használata: Csomagok kezelése

## Áttekintés
Az `apt` parancs a Debian-alapú rendszerek csomagkezelője, amely lehetővé teszi a szoftverek telepítését, frissítését és eltávolítását. Az `apt` egyszerűsíti a csomagkezelési folyamatokat, és kényelmes megoldást nyújt a felhasználók számára a rendszer karbantartásához.

## Használat
A `apt` parancs alapvető szintaxisa a következő:

```bash
apt [opciók] [argumentumok]
```

## Gyakori Opciók
- `install`: Csomag telepítése.
- `remove`: Csomag eltávolítása.
- `update`: A csomaglisták frissítése.
- `upgrade`: A telepített csomagok frissítése.
- `search`: Csomag keresése a tárolókban.

## Gyakori Példák
- Csomag telepítése:
    ```bash
    sudo apt install <csomag_neve>
    ```
  
- Csomag eltávolítása:
    ```bash
    sudo apt remove <csomag_neve>
    ```

- Csomaglisták frissítése:
    ```bash
    sudo apt update
    ```

- Telepített csomagok frissítése:
    ```bash
    sudo apt upgrade
    ```

- Csomag keresése:
    ```bash
    apt search <keresési_kifejezés>
    ```

## Tippek
- Mindig futtassuk a `sudo apt update` parancsot a csomagok telepítése előtt, hogy biztosak legyünk a legfrissebb verziókban.
- Használjuk a `-y` opciót a nem interaktív telepítéshez, például: `sudo apt install -y <csomag_neve>`.
- Rendszeresen ellenőrizzük a nem használt csomagokat a `sudo apt autoremove` parancs segítségével, hogy tisztán tartsuk a rendszert.