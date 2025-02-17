# [Linux] Bash curl használata: Weboldalak lekérése

## Áttekintés
A `curl` parancs egy parancssori eszköz, amely lehetővé teszi a felhasználók számára, hogy adatokat küldjenek és fogadjanak URL-ek segítségével. Leggyakrabban weboldalak, API-k és fájlok letöltésére használják.

## Használat
A `curl` parancs alapvető szintaxisa a következő:

```bash
curl [opciók] [argumentumok]
```

## Gyakori opciók
- `-O`: A letöltött fájlt a megadott néven menti.
- `-L`: Követi a HTTP átirányításokat.
- `-d`: Adatokat küld POST kérésben.
- `-H`: Egyéni HTTP fejlécet ad meg.
- `-u`: Felhasználónév és jelszó megadása az alapértelmezett hitelesítéshez.

## Gyakori példák
1. **Weboldal letöltése**:
   ```bash
   curl https://www.example.com
   ```

2. **Fájl letöltése a megadott néven**:
   ```bash
   curl -O https://www.example.com/file.zip
   ```

3. **HTTP átirányítás követése**:
   ```bash
   curl -L https://bit.ly/example
   ```

4. **Adatok küldése POST kérésben**:
   ```bash
   curl -d "name=John&age=30" https://www.example.com/api
   ```

5. **Egyéni HTTP fejléc megadása**:
   ```bash
   curl -H "Authorization: Bearer TOKEN" https://www.example.com/api
   ```

## Tippek
- Mindig ellenőrizd a letöltött fájlok integritását, ha fontos adatokat tartalmaznak.
- Használj `-v` (verbose) opciót a részletes kimenethez, ha hibakeresésre van szükséged.
- A `curl` parancsot gyakran használják scripteléshez, így érdemes automatizálni a folyamatokat.