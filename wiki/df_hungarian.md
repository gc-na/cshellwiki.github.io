# [Linux] Bash df használata: A lemezterület ellenőrzése

## Áttekintés
A `df` parancs a fájlrendszerek lemezterületének használatát mutatja meg. Segítségével gyorsan ellenőrizhetjük, hogy mennyi szabad, használt és összes terület áll rendelkezésre a csatlakoztatott fájlrendszerekben.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
df [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Az eredmények emberi olvasható formátumban jelennek meg (pl. MB, GB).
- `-T`: Megjeleníti a fájlrendszer típusát is.
- `-a`: Megjeleníti a nullával rendelkező fájlrendszereket is.
- `-i`: A fájlrendszer inode-ainak használatát mutatja meg.

## Gyakori példák

1. **Alapvető lemezhasználat megjelenítése:**
   ```bash
   df
   ```

2. **Emberi olvasható formátumban:**
   ```bash
   df -h
   ```

3. **Fájlrendszer típusának megjelenítése:**
   ```bash
   df -T
   ```

4. **Inode használat ellenőrzése:**
   ```bash
   df -i
   ```

5. **Minden fájlrendszer megjelenítése, beleértve a nullával rendelkezőket is:**
   ```bash
   df -a
   ```

## Tippek
- Használja a `-h` opciót, hogy könnyebben értelmezhető formátumban lássa az eredményeket.
- Rendszeresen ellenőrizze a lemezterületet, hogy elkerülje a fájlrendszer megtelését.
- A `df` parancsot kombinálhatja más parancsokkal, mint például a `grep`, hogy csak a kívánt fájlrendszereket jelenítse meg.