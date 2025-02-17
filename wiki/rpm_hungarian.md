# [Linux] Bash rpm használata: Csomagkezelés és telepítés

## Áttekintés
Az `rpm` (Red Hat Package Manager) egy csomagkezelő eszköz, amely lehetővé teszi a szoftvercsomagok telepítését, eltávolítását és kezelését Linux rendszereken, különösen a Red Hat alapú disztribúciókban.

## Használat
Az `rpm` parancs alapvető szintaxisa a következő:

```bash
rpm [opciók] [argumentumok]
```

## Gyakori Opciók
- `-i`: Telepít egy új csomagot.
- `-e`: Eltávolít egy telepített csomagot.
- `-q`: Lekérdezi a telepített csomagokat.
- `-U`: Frissít egy telepített csomagot.
- `-v`: Verbose (részletes) kimenetet ad.
- `--help`: Megjeleníti a parancs súgóját.

## Gyakori Példák
1. **Csomag telepítése:**
   ```bash
   rpm -i csomag.rpm
   ```

2. **Csomag eltávolítása:**
   ```bash
   rpm -e csomag_neve
   ```

3. **Telepített csomagok listázása:**
   ```bash
   rpm -qa
   ```

4. **Csomag frissítése:**
   ```bash
   rpm -U csomag.rpm
   ```

5. **Csomag információk lekérdezése:**
   ```bash
   rpm -qi csomag_neve
   ```

## Tippek
- Mindig ellenőrizd a csomag függőségeit telepítés előtt, hogy elkerüld a hiányzó könyvtárakat.
- Használj `-v` opciót a részletes kimenethez, hogy jobban megértsd a telepítési folyamatot.
- A csomagok eltávolítása előtt győződj meg arról, hogy nem használja őket más alkalmazás.