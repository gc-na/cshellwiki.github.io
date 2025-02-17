# [Linux] Bash htop használata: Rendszerfolyamatok valós idejű megjelenítése

## Áttekintés
A `htop` egy interaktív folyamatkezelő eszköz, amely lehetővé teszi a felhasználók számára, hogy valós időben figyeljék és kezeljék a rendszerfolyamatokat. A `htop` grafikus felülettel rendelkezik, amely megkönnyíti a folyamatok áttekintését és kezelését, ellentétben a hagyományos `top` parancssal.

## Használat
A `htop` parancs alapvető szintaxisa a következő:

```bash
htop [opciók] [érvek]
```

## Gyakori opciók
- `-d, --delay`: Beállítja a frissítési késleltetést másodpercekben.
- `-u, --user`: Csak a megadott felhasználó folyamatainak megjelenítése.
- `-p, --pid`: Csak a megadott PID-ű folyamatok megjelenítése.
- `-s, --sort-key`: A megjelenített folyamatok rendezési kulcsa (pl. `pid`, `mem`, `cpu`).

## Gyakori példák
1. **Alapértelmezett indítás**:
   ```bash
   htop
   ```

2. **Frissítési késleltetés beállítása 2 másodpercre**:
   ```bash
   htop -d 2
   ```

3. **Csak egy adott felhasználó folyamatainak megjelenítése**:
   ```bash
   htop -u felhasználónév
   ```

4. **Csak egy adott PID-ű folyamat megjelenítése**:
   ```bash
   htop -p 1234
   ```

5. **Folyamatok rendezése CPU használat szerint**:
   ```bash
   htop -s cpu
   ```

## Tippek
- Használja a nyilakat a folyamatok közötti navigáláshoz, és az `F9` billentyűt a folyamatok leállításához.
- A `F2` billentyű megnyomásával hozzáférhet a beállításokhoz, ahol testreszabhatja a megjelenítést.
- Használja a `F3` billentyűt a kereséshez, hogy gyorsan megtalálja a kívánt folyamatot.
- A `F10` billentyűvel gyorsan kiléphet a `htop`-ból.