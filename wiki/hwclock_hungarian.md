# [Linux] Bash hwclock használata: Az időjárás és a rendszeridő kezelése

## Áttekintés
A `hwclock` parancs a hardveróra (RTC - Real Time Clock) beállítására és lekérdezésére szolgál. Ezzel a paranccsal megtekinthetjük a rendszer időpontját és dátumát, valamint szinkronizálhatjuk a rendszeridőt a hardverórával.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
hwclock [opciók] [argumentumok]
```

## Gyakori Opciók
- `--show`: Megjeleníti a hardveróra aktuális időpontját.
- `--set`: Beállítja a hardveróra időpontját.
- `--systohc`: A rendszeridőt beállítja a hardverórára.
- `--hctosys`: A hardveróra időpontját beállítja a rendszeridőre.
- `--utc`: Az időzónát UTC-ra állítja.

## Gyakori Példák
1. A hardveróra aktuális időpontjának megjelenítése:
   ```bash
   hwclock --show
   ```

2. A rendszeridő beállítása a hardverórára:
   ```bash
   hwclock --systohc
   ```

3. A hardveróra időpontjának beállítása:
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

4. A hardveróra időpontjának beállítása a rendszeridőre:
   ```bash
   hwclock --hctosys
   ```

## Tippek
- Mindig ellenőrizd a hardveróra időpontját, mielőtt szinkronizálnád a rendszeridőt.
- Használj `sudo`-t, ha a parancs végrehajtásához rendszergazdai jogosultságokra van szükséged.
- Rendszeres időközönként szinkronizáld a hardverórát, hogy elkerüld az időeltéréseket.