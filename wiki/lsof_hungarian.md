# [Linux] Bash lsof használata: Fájlok és folyamatok nyomon követése

## Áttekintés
Az `lsof` (List Open Files) parancs lehetővé teszi a felhasználók számára, hogy megtekintsék a nyitott fájlokat és azokhoz kapcsolódó folyamatokat a rendszerükön. Ez különösen hasznos lehet a rendszerdiagnosztikában és a hibaelhárításban.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
lsof [opciók] [argumentumok]
```

## Gyakori Opciók
- `-i`: Megjeleníti a hálózati kapcsolatokhoz kapcsolódó nyitott fájlokat.
- `-u [felhasználónév]`: Csak a megadott felhasználó által nyitott fájlokat listázza.
- `-p [PID]`: Csak a megadott folyamat azonosítójához (PID) tartozó fájlokat jeleníti meg.
- `+D [könyvtár]`: Rekurzívan listázza a megadott könyvtárban található fájlokat.
- `-t`: Csak a folyamat azonosítókat (PID) jeleníti meg, a fájlok nevei nélkül.

## Gyakori Példák
1. **Minden nyitott fájl listázása:**
   ```bash
   lsof
   ```

2. **Nyitott fájlok megjelenítése egy adott felhasználóhoz:**
   ```bash
   lsof -u username
   ```

3. **Hálózati kapcsolatok megjelenítése:**
   ```bash
   lsof -i
   ```

4. **Folyamatok listázása egy adott PID-hez:**
   ```bash
   lsof -p 1234
   ```

5. **Fájlok listázása egy adott könyvtárban:**
   ```bash
   lsof +D /path/to/directory
   ```

## Tippek
- Használja a `-t` opciót, ha csak a PID-ekre van szüksége, például egy folyamat leállításához.
- A `lsof` parancsot rendszergazdai jogosultságokkal futtatva (sudo) több információt kaphat a rendszer összes folyamatáról.
- Kombinálja az opciókat a részletesebb információkért, például `lsof -i -u username` a felhasználó hálózati kapcsolatairól.