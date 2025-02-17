# [Linux] Bash killall használata: Folyamatok leállítása név alapján

## Áttekintés
A `killall` parancs lehetővé teszi, hogy egy adott névvel rendelkező folyamatokat állítsunk le a rendszerben. Ez a parancs hasznos, ha több példányt futtatunk egy programból, és mindet egyszerre szeretnénk leállítani.

## Használat
A `killall` parancs alapvető szintaxisa a következő:

```bash
killall [opciók] [argumentumok]
```

## Gyakori opciók
- `-u [felhasználó]`: Csak a megadott felhasználó által indított folyamatokat állítja le.
- `-I`: Figyelmen kívül hagyja a kis- és nagybetűk közötti különbséget a folyamat nevében.
- `-q`: Csendes mód, amely nem ad visszajelzést a leállított folyamatokról.
- `-9`: Azonnali leállítás, amely nem engedélyezi a folyamat számára, hogy tisztán befejezze a működését.

## Gyakori példák
1. Minden `firefox` folyamat leállítása:
   ```bash
   killall firefox
   ```

2. Csak a `gedit` folyamatok leállítása egy adott felhasználó esetén:
   ```bash
   killall -u felhasználó gedit
   ```

3. Minden `java` folyamat leállítása, figyelmen kívül hagyva a kis- és nagybetűk közötti különbséget:
   ```bash
   killall -I java
   ```

4. Minden `myapp` folyamat azonnali leállítása:
   ```bash
   killall -9 myapp
   ```

## Tippek
- Mindig ellenőrizd, hogy milyen folyamatokat állítasz le, hogy elkerüld a fontos rendszerszolgáltatások véletlen leállítását.
- Használj `-q` opciót, ha nem szeretnél zavaró üzeneteket a parancs végrehajtása után.
- A `killall` parancs használata előtt érdemes lehet a `pgrep` parancsot használni, hogy megnézd, mely folyamatok futnak a megadott névvel.