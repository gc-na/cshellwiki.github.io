# [Linux] Bash timedatectl használata: Idő és dátum beállítása

## Áttekintés
A `timedatectl` parancs a rendszer idő- és dátumbeállításainak kezelésére szolgál. Ezen kívül lehetővé teszi az időzónák kezelését és az NTP (Network Time Protocol) szinkronizálás beállítását is.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
timedatectl [opciók] [érvek]
```

## Gyakori opciók
- `set-time`: Beállítja a rendszert az adott időre.
- `set-timezone`: Megváltoztatja a rendszer időzónáját.
- `set-ntp`: Engedélyezi vagy letiltja az NTP szinkronizálást.
- `status`: Megjeleníti a jelenlegi idő- és dátumbeállításokat.

## Gyakori példák
1. **A rendszer időjének beállítása:**
   ```bash
   timedatectl set-time '2023-10-01 12:00:00'
   ```

2. **Időzóna megváltoztatása:**
   ```bash
   timedatectl set-timezone Europe/Budapest
   ```

3. **NTP szinkronizálás engedélyezése:**
   ```bash
   timedatectl set-ntp true
   ```

4. **A jelenlegi idő- és dátumbeállítások megjelenítése:**
   ```bash
   timedatectl status
   ```

## Tippek
- Mindig ellenőrizd a rendszer időzónáját a `status` paranccsal, mielőtt időt vagy dátumot állítanál be.
- Használj pontos formátumot az idő és dátum beállításához, hogy elkerüld a hibákat.
- Ha NTP-t használsz, győződj meg róla, hogy a hálózati kapcsolat stabil, hogy a szinkronizálás zökkenőmentes legyen.