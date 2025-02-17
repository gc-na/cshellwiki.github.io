# [Linux] Bash scp használata: Fájlok biztonságos másolása távoli gépekre

## Áttekintés
Az `scp` (Secure Copy Protocol) parancs lehetővé teszi fájlok biztonságos másolását egy helyi és egy távoli gép között SSH protokoll használatával. Az `scp` parancs titkosítja az adatokat, így védve van a lehallgatás ellen.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
scp [opciók] [forrás] [cél]
```

## Gyakori opciók
- `-r`: Rekurzív másolás könyvtárak esetén.
- `-P`: A távoli gép portjának megadása (nagy P, mert a kis p az SSH protokollban van).
- `-i`: Az SSH kulcs fájl megadása.
- `-v`: Verbose (részletes) mód, amely megjeleníti a másolás folyamatát.

## Gyakori példák
1. **Fájl másolása a helyi gépről a távoli gépre:**
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. **Fájl másolása a távoli gépről a helyi gépre:**
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. **Könyvtár rekurzív másolása a távoli gépre:**
   ```bash
   scp -r /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
   ```

4. **Másolás egy nem alapértelmezett porton:**
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tippek
- Mindig ellenőrizd, hogy a távoli gép elérhető-e, mielőtt másolni próbálnál.
- Használj SSH kulcsot a hitelesítéshez, hogy elkerüld a jelszó megadását minden alkalommal.
- A `-v` opció segíthet a hibaelhárításban, ha problémák merülnek fel a másolás során.