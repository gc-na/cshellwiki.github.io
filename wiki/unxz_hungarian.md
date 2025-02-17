# [Linux] Bash unxz használata: Fájlok kicsomagolása

## Áttekintés
Az `unxz` parancs a `.xz` kiterjesztésű fájlok kicsomagolására szolgál. Ez a parancs a XZ tömörítési algoritmus által létrehozott fájlok visszaállítására használható, lehetővé téve a felhasználók számára, hogy az eredeti fájlokat visszanyerjék.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
unxz [opciók] [fájlok]
```

## Gyakori opciók
- `-k` vagy `--keep`: Megőrzi az eredeti `.xz` fájlt a kicsomagolás után.
- `-f` vagy `--force`: Kényszeríti a kicsomagolást, még ha a célfájl már létezik is.
- `-v` vagy `--verbose`: Részletes kimenetet ad a kicsomagolás folyamatáról.

## Gyakori példák
1. **Alap kicsomagolás**:
   ```bash
   unxz fájl.xz
   ```

2. **Eredeti fájl megőrzése**:
   ```bash
   unxz -k fájl.xz
   ```

3. **Kényszerített kicsomagolás**:
   ```bash
   unxz -f fájl.xz
   ```

4. **Részletes kimenet megjelenítése**:
   ```bash
   unxz -v fájl.xz
   ```

## Tippek
- Mindig ellenőrizd, hogy a kicsomagolt fájlok nem felülírják-e a meglévő fájlokat, ha nem használod a `-k` opciót.
- Használj `-v` opciót, ha szeretnéd nyomon követni a kicsomagolás folyamatát, különösen nagy fájlok esetén.
- A `unxz` parancs használata előtt győződj meg róla, hogy a fájl valóban `.xz` formátumú, hogy elkerüld a hibákat.