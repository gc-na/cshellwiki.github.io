# [Linux] Bash w használata: Aktív felhasználók és rendszerinformációk megjelenítése

## Áttekintés
A `w` parancs megjeleníti a rendszerre bejelentkezett felhasználók listáját, valamint információkat nyújt az aktuális tevékenységükről és a rendszer állapotáról. Hasznos eszköz a rendszeradminisztrátorok számára, hogy nyomon követhessék a felhasználói aktivitást.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
w [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: A fejléc eltávolítása a kimenetből.
- `-s`: Rövidített formátum, amely kevesebb információt jelenít meg.
- `-u`: Csak a bejelentkezett felhasználók listáját mutatja.

## Gyakori példák
1. **Alapértelmezett használat**: A `w` parancs egyszerű futtatása megjeleníti az összes bejelentkezett felhasználót és azok aktivitását.
   ```bash
   w
   ```

2. **Fejléc eltávolítása**: A `-h` opcióval eltávolíthatjuk a fejlécet a kimenetből.
   ```bash
   w -h
   ```

3. **Rövidített formátum**: A `-s` opció használatával kevesebb információt kapunk.
   ```bash
   w -s
   ```

4. **Csak bejelentkezett felhasználók**: Az `-u` opcióval csak a felhasználók listáját jeleníthetjük meg.
   ```bash
   w -u
   ```

## Tippek
- Használja a `w` parancsot rendszeres időközönként, hogy nyomon követhesse a felhasználói aktivitást.
- Kombinálja a `w` parancsot más parancsokkal, mint például a `grep`, hogy szűkítse a kimenetet egy adott felhasználóra.
- Figyelje a rendszer terhelését és a felhasználói aktivitást, hogy optimalizálja a rendszer teljesítményét.