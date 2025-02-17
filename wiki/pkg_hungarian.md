# [Linux] Bash pkg használata: Csomagkezelő parancs

## Áttekintés
A `pkg` parancs egy csomagkezelő eszköz, amely lehetővé teszi a szoftvercsomagok telepítését, eltávolítását és kezelését a rendszeren. Ezzel a paranccsal egyszerűen kezelhetjük a telepített alkalmazásokat és azok függőségeit.

## Használat
A `pkg` parancs alapvető szintaxisa a következő:

```bash
pkg [opciók] [argumentumok]
```

## Gyakori opciók
- `install`: Új csomag telepítése.
- `remove`: Csomag eltávolítása.
- `update`: A csomaglista frissítése.
- `upgrade`: Telepített csomagok frissítése a legújabb verzióra.
- `search`: Csomag keresése a tárolókban.

## Gyakori példák
1. Csomag telepítése:
   ```bash
   pkg install csomagneve
   ```

2. Csomag eltávolítása:
   ```bash
   pkg remove csomagneve
   ```

3. Csomaglista frissítése:
   ```bash
   pkg update
   ```

4. Telepített csomagok frissítése:
   ```bash
   pkg upgrade
   ```

5. Csomag keresése:
   ```bash
   pkg search keresett_csomag
   ```

## Tippek
- Mindig futtassuk a `pkg update` parancsot a csomagok telepítése előtt, hogy biztosak legyünk benne, hogy a legfrissebb verziókat telepítjük.
- Használjunk `pkg search` parancsot, hogy gyorsan megtaláljuk a szükséges csomagokat.
- Ellenőrizzük a telepített csomagok listáját a `pkg info` paranccsal, hogy lássuk, mi van a rendszerünkön.