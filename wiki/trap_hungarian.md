# [Linux] Bash trap használata: A jelek kezelése

## Áttekintés
A `trap` parancs lehetővé teszi a Bash szkriptek számára, hogy reagáljanak bizonyos jelekre vagy eseményekre, például a folyamat leállítására vagy megszakítására. Ezzel a parancsal megadhatjuk, hogy mit tegyen a szkript, amikor egy adott jel érkezik.

## Használat
A `trap` parancs alapvető szintaxisa a következő:

```bash
trap [opciók] [argumentumok]
```

## Gyakori opciók
- `SIGINT`: A Ctrl+C által generált jel.
- `SIGTERM`: A folyamat leállítására szolgáló jel.
- `EXIT`: A szkript befejezésekor végrehajtandó parancsok.
- `ERR`: Hibák esetén végrehajtandó parancsok.

## Gyakori példák

1. **Alapvető jelkezelés**:
   A következő példa megmutatja, hogyan lehet kezelni a Ctrl+C jelet, hogy a szkript ne álljon le, hanem egy üzenetet írjon ki:
   ```bash
   trap 'echo "A folyamat megszakítva."' SIGINT
   while true; do
       echo "Folyamatban..."
       sleep 1
   done
   ```

2. **Folyamat leállítása**:
   A következő példa megmutatja, hogyan lehet a `SIGTERM` jelet kezelni, hogy a szkript tisztán befejezze a munkáját:
   ```bash
   trap 'echo "A folyamat leállítása..."; exit' SIGTERM
   while true; do
       echo "Folyamatban..."
       sleep 1
   done
   ```

3. **Hibakezelés**:
   A `trap` használható hibák kezelésére is:
   ```bash
   trap 'echo "Hiba történt!"; exit 1' ERR
   false  # Ez a parancs hibát generál
   ```

## Tippek
- Mindig érdemes a `trap` parancsot a szkript elején definiálni, hogy a jelek kezelésére már a szkript indításakor készen álljon.
- Használj világos és érthető üzeneteket a `trap` parancsban, hogy könnyen nyomon követhesd a szkript viselkedését.
- Teszteld a szkriptedet különböző jelek küldésével, hogy biztos lehess benne, hogy a `trap` megfelelően működik.