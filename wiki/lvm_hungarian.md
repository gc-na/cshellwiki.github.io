# [Linux] Bash lvm használata: Lemezkezelés és kötetkezelés

## Áttekintés
Az `lvm` (Logical Volume Manager) parancs lehetővé teszi a logikai kötetek kezelését a Linux operációs rendszerekben. Segítségével dinamikusan kezelhetjük a tárolóeszközöket, lehetővé téve a kötetek létrehozását, módosítását és törlését.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
lvm [opciók] [argumentumok]
```

## Gyakori Opciók
- `create`: Új logikai kötet létrehozása.
- `remove`: Logikai kötet eltávolítása.
- `extend`: Logikai kötet méretének növelése.
- `reduce`: Logikai kötet méretének csökkentése.
- `lvdisplay`: A logikai kötetek részleteinek megjelenítése.

## Gyakori Példák
1. **Új logikai kötet létrehozása**:
   ```bash
   lvm create -n my_volume -L 10G my_volume_group
   ```

2. **Logikai kötet eltávolítása**:
   ```bash
   lvm remove my_volume
   ```

3. **Logikai kötet méretének növelése**:
   ```bash
   lvm extend -L +5G my_volume
   ```

4. **Logikai kötet méretének csökkentése**:
   ```bash
   lvm reduce -L -5G my_volume
   ```

5. **Logikai kötetek részleteinek megjelenítése**:
   ```bash
   lvm lvdisplay
   ```

## Tippek
- Mindig készítsünk biztonsági másolatot a fontos adatainkról, mielőtt módosítanánk a köteteket.
- Használjunk `lvm` parancsokat root jogosultságokkal a megfelelő működés érdekében.
- Rendszeresen ellenőrizzük a logikai kötetek állapotát a `lvdisplay` paranccsal, hogy elkerüljük a váratlan problémákat.