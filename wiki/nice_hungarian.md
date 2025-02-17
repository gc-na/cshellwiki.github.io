# [Linux] Bash nice használata: A folyamatok prioritásának beállítása

## Áttekintés
A `nice` parancs a Linux és Unix rendszerekben lehetővé teszi a folyamatok prioritásának beállítását. Ezzel a paranccsal csökkenthetjük egy folyamat CPU-hoz való hozzáférésének prioritását, így más folyamatok számára több erőforrást biztosíthatunk.

## Használat
A `nice` parancs alapvető szintaxisa a következő:

```bash
nice [opciók] [parancs] [argumentumok]
```

## Gyakori opciók
- `-n, --adjustment`: A prioritás módosítása. A szám negatív értéke növeli a prioritást, míg a pozitív csökkenti.
- `-h, --help`: Segítséget nyújt a parancs használatához.
- `-v, --version`: Megjeleníti a `nice` parancs verzióját.

## Gyakori példák
1. **Alapértelmezett prioritás beállítása**:
   ```bash
   nice -n 10 myscript.sh
   ```
   Ez a parancs a `myscript.sh` futtatását 10-es prioritással indítja.

2. **Folyamat prioritásának csökkentése**:
   ```bash
   nice -n 19 myheavyprocess
   ```
   A `myheavyprocess` 19-es prioritással fut, így más folyamatok számára több CPU-időt biztosít.

3. **Folyamat indítása alapértelmezett prioritással**:
   ```bash
   nice mycommand
   ```
   A `mycommand` alapértelmezett prioritással indul, ami általában 0.

## Tippek
- Használj alacsonyabb prioritást (nagyobb számot) olyan folyamatokhoz, amelyek nem sürgősek, hogy más fontosabb feladatoknak több erőforrást biztosíts.
- Ellenőrizd a folyamatok prioritását a `top` vagy `htop` parancs segítségével, hogy lásd, hogyan befolyásolja a `nice` a rendszer teljesítményét.
- Ne feledd, hogy a `nice` parancs csak a folyamat indításakor állítja be a prioritást; a már futó folyamatok prioritását a `renice` paranccsal módosíthatod.