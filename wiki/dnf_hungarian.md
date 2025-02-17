# [Linux] Bash dnf használat: Csomagkezelő parancs

## Áttekintés
A `dnf` (Dandified YUM) egy csomagkezelő parancs, amelyet a Fedora és más RPM-alapú disztribúciók használnak. Fő célja a szoftvercsomagok telepítése, frissítése és eltávolítása, valamint a rendszer csomagjaival kapcsolatos információk kezelése.

## Használat
A `dnf` parancs alapvető szintaxisa a következő:

```bash
dnf [opciók] [argumentumok]
```

## Gyakori opciók
- `install`: Csomag telepítése.
- `remove`: Csomag eltávolítása.
- `update`: Telepített csomagok frissítése.
- `search`: Csomagok keresése név vagy leírás alapján.
- `info`: Információk megjelenítése egy csomagról.

## Gyakori példák
- Csomag telepítése:
  ```bash
  dnf install csomagneve
  ```

- Csomag eltávolítása:
  ```bash
  dnf remove csomagneve
  ```

- Telepített csomagok frissítése:
  ```bash
  dnf update
  ```

- Csomag keresése:
  ```bash
  dnf search keresett_kifejezés
  ```

- Csomag információinak megjelenítése:
  ```bash
  dnf info csomagneve
  ```

## Tippek
- Mindig érdemes frissíteni a csomaglistát a `dnf update` parancs futtatásával, mielőtt új csomagokat telepítenél.
- Használj `-y` opciót a parancsok végrehajtásához anélkül, hogy megerősítést kérne:
  ```bash
  dnf install -y csomagneve
  ```
- Ellenőrizd a telepített csomagok listáját a `dnf list installed` paranccsal, hogy tudd, mi van a rendszereden.