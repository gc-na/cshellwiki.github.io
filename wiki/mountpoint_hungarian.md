# [Linux] Bash mountpoint használata: Ellenőrzi, hogy egy könyvtár csatlakoztatott-e

## Áttekintés
A `mountpoint` parancs arra szolgál, hogy ellenőrizze, vajon egy adott könyvtár csatlakoztatott-e fájlrendszerhez. Hasznos eszköz a rendszeradminisztrátorok számára, hogy gyorsan megállapítsák, hogy egy könyvtár valóban mountolt-e.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
mountpoint [opciók] [argumentumok]
```

## Gyakori Opciók
- `-q`: Csendes üzemmód, nem ad vissza üzenetet, csak a visszatérési kódot ellenőrzi.
- `-d`: Kimenet részletesebb információkat tartalmaz a mountpontról.

## Gyakori Példák
1. Ellenőrizd, hogy a `/mnt/data` könyvtár csatlakoztatott-e:
   ```bash
   mountpoint /mnt/data
   ```

2. Csendes üzemmódban ellenőrizd a `/media/usb` mountpontot:
   ```bash
   mountpoint -q /media/usb
   ```

3. Részletes információk megjelenítése a `/home/user` könyvtárról:
   ```bash
   mountpoint -d /home/user
   ```

## Tippek
- Használj csendes üzemmódot, ha csak a visszatérési kódra van szükséged, például scriptelés során.
- Ellenőrizd a mountpontokat rendszeresen, hogy elkerüld a fájlrendszerrel kapcsolatos problémákat.
- Használj részletes opciót, ha több információra van szükséged a mountpont állapotáról.