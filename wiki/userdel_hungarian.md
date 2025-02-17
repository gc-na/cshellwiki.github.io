# [Linux] Bash userdel használata: Felhasználók törlése

## Áttekintés
A `userdel` parancs a Linux rendszerekben felhasználók törlésére szolgál. Ezzel a paranccsal eltávolíthatjuk a rendszerből a nem kívánt felhasználói fiókokat.

## Használat
A `userdel` parancs alapvető szintaxisa a következő:

```bash
userdel [opciók] [felhasználónév]
```

## Gyakori opciók
- `-r`: Eltávolítja a felhasználóhoz tartozó otthoni könyvtárat és a levelezési fájlokat is.
- `-f`: Kényszeríti a felhasználó törlését, még akkor is, ha az be van jelentkezve.
- `-Z`: A SELinux kontextusának eltávolítása a felhasználó törlésekor.

## Gyakori példák
1. **Felhasználó törlése otthoni könyvtár nélkül:**
   ```bash
   userdel felhasználónév
   ```

2. **Felhasználó törlése otthoni könyvtárral:**
   ```bash
   userdel -r felhasználónév
   ```

3. **Felhasználó kényszerített törlése:**
   ```bash
   userdel -f felhasználónév
   ```

4. **Felhasználó törlése SELinux kontextussal:**
   ```bash
   userdel -Z felhasználónév
   ```

## Tippek
- Mindig ellenőrizd, hogy a törölni kívánt felhasználó nem aktív-e, hogy elkerüld a problémákat.
- Használj biztonsági másolatot a felhasználói adatok megőrzésére, mielőtt törölnéd a fiókot.
- A `-r` opció használatakor légy óvatos, mivel ez véglegesen eltávolítja a felhasználó összes fájlját.