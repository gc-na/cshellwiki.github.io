# [Linux] Bash write használata: Üzenet küldése más felhasználóknak

## Áttekintés
A `write` parancs lehetővé teszi, hogy üzeneteket küldjünk más felhasználóknak a rendszerben. Ez a parancs közvetlen kapcsolatot teremt a felhasználók között, lehetővé téve, hogy valós időben kommunikáljanak egymással.

## Használat
A `write` parancs alapvető szintaxisa a következő:

```bash
write [felhasználónév] [tty]
```

A `tty` paraméter opcionális, és általában nem szükséges, ha a felhasználó egyetlen terminálon van bejelentkezve.

## Gyakori opciók
- `-n`: Csak a felhasználó nevét írja ki, nem a tty-t.
- `-s`: Csendes üzenetküldés, nem jeleníti meg a felhasználónál az üzenetet, csak a terminálon.

## Gyakori példák
1. Üzenet küldése egy másik felhasználónak:
   ```bash
   write jozsi
   Hello Jozsi, hogyan vagy?
   ```

2. Üzenet küldése egy másik terminálra:
   ```bash
   write jozsi pts/1
   Éppen dolgozom, később beszéljünk!
   ```

3. Csendes üzenet küldése:
   ```bash
   write -s jozsi
   Kérlek, nézd meg az e-mailemet!
   ```

## Tippek
- Ellenőrizd, hogy a címzett felhasználó be van-e jelentkezve, különben nem fogja megkapni az üzenetet.
- Használj rövid és világos üzeneteket, hogy a kommunikáció hatékony legyen.
- Ne felejtsd el, hogy a `write` parancs valós időben működik, így a címzett azonnal láthatja az üzenetet, amint azt elküldted.