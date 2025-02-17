# [Linux] Bash vigr használat: Szövegszerkesztő a /etc/passwd fájlhoz

## Áttekintés
A `vigr` parancs egy biztonságos szövegszerkesztő, amelyet a `/etc/passwd` és `/etc/group` fájlok szerkesztésére használnak. Ez a parancs megakadályozza, hogy párhuzamosan több felhasználó szerkessze ezeket a fájlokat, így elkerülve a potenciális adatvesztést vagy -károsodást.

## Használat
A `vigr` parancs alapvető szintaxisa a következő:

```bash
vigr [opciók] [fájl]
```

## Gyakori opciók
- `-f, --file`: Megadja a szerkesztendő fájlt (alapértelmezett: `/etc/passwd`).
- `-s, --safe`: Biztonságos módban indítja a szerkesztőt, amely megakadályozza a fájlok párhuzamos szerkesztését.
- `-h, --help`: Megjeleníti a súgót a parancs használatáról.

## Gyakori példák
1. A `/etc/passwd` fájl megnyitása szerkesztésre:
   ```bash
   vigr
   ```

2. A `/etc/group` fájl megnyitása:
   ```bash
   vigr -f /etc/group
   ```

3. A fájl biztonságos módú szerkesztése:
   ```bash
   vigr -s
   ```

## Tippek
- Mindig használj `vigr`-t a `/etc/passwd` és `/etc/group` fájlok szerkesztésére, hogy elkerüld a fájlok sérülését.
- Ellenőrizd a fájl tartalmát a szerkesztés előtt, hogy tisztában legyél a módosítások hatásával.
- Használj biztonsági másolatot a fájlokról, mielőtt bármilyen jelentős változtatást végeznél.