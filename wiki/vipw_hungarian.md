# [Linux] Bash vipw használat: Felhasználói fiókok szerkesztése

## Áttekintés
A `vipw` parancs lehetővé teszi a felhasználói fiókok és jelszavak biztonságos szerkesztését a `/etc/passwd` és `/etc/shadow` fájlokban. A parancs megnyitja ezeket a fájlokat egy szövegszerkesztőben, miközben biztosítja, hogy más folyamatok ne férjenek hozzá a fájlokhoz, így elkerülve a versenyhelyzeteket.

## Használat
A `vipw` parancs alapvető szintaxisa a következő:

```bash
vipw [opciók]
```

## Gyakori opciók
- `-s`: A `vipw` parancs a `/etc/shadow` fájl szerkesztésére nyílik meg.
- `-u`: A felhasználói fiókokat a `/etc/passwd` fájlban szerkeszti.
- `-h`: Segítséget nyújt a parancs használatához.

## Gyakori példák
1. A felhasználói fiókok szerkesztése:
   ```bash
   vipw
   ```

2. A jelszó fájl szerkesztése:
   ```bash
   vipw -s
   ```

3. A felhasználói fiókok szerkesztése egy adott szövegszerkesztővel (például `nano`):
   ```bash
   EDITOR=nano vipw
   ```

## Tippek
- Mindig készíts biztonsági másolatot a fájlokról, mielőtt módosítanád őket.
- Használj egy megbízható szövegszerkesztőt, amely ismeri a UNIX formátumot.
- Ellenőrizd a fájlok szintaxisát a módosítások után, hogy elkerüld a rendszerindítási problémákat.