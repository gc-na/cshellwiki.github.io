# [Linux] Bash tput használata: A terminál megjelenítésének vezérlése

## Áttekintés
A `tput` parancs a terminálok megjelenítésének és működésének vezérlésére szolgál. Lehetővé teszi a felhasználók számára, hogy különböző terminál-specifikus beállításokat alkalmazzanak, például színek, kurzor pozíciók és egyéb formázási lehetőségek beállítását.

## Használat
A `tput` parancs alapvető szintaxisa a következő:

```bash
tput [opciók] [argumentumok]
```

## Gyakori opciók
- `setaf [szám]`: Beállítja a szöveg elülső színét.
- `setab [szám]`: Beállítja a háttér színét.
- `clear`: Törli a terminál képernyőjét.
- `cup [sor] [oszlop]`: A kurzort a megadott sorra és oszlopra helyezi.
- `bold`: A szöveget félkövérre állítja.

## Gyakori példák
1. **Szöveg színének beállítása**:
   ```bash
   tput setaf 1; echo "Ez piros szöveg."
   ```

2. **Háttérszín beállítása**:
   ```bash
   tput setab 4; echo "Ez kék háttérrel rendelkezik."
   ```

3. **Képernyő törlése**:
   ```bash
   tput clear
   ```

4. **Kurzor pozicionálása**:
   ```bash
   tput cup 10 20; echo "A kurzor itt van."
   ```

5. **Félkövér szöveg**:
   ```bash
   tput bold; echo "Ez félkövér szöveg."
   ```

## Tippek
- A `tput` parancs használata előtt érdemes ellenőrizni, hogy a terminál támogatja-e a kívánt színeket és formázásokat.
- A színek és formázások számát a terminál típusa határozza meg; érdemes kísérletezni a különböző opciókkal.
- A `tput` parancsot script-ekben is használhatod, hogy a terminál megjelenését dinamikusan módosítsd.