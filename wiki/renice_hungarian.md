# [Linux] Bash renice használata: A folyamat prioritásának módosítása

## Áttekintés
A `renice` parancs lehetővé teszi a futó folyamatok prioritásának módosítását a Linux operációs rendszerben. Ezzel a parancssal növelhetjük vagy csökkenthetjük a folyamatok prioritását, ami befolyásolja azok CPU-hoz való hozzáférését.

## Használat
A `renice` parancs alapvető szintaxisa a következő:

```bash
renice [opciók] [prioritás] [PID]
```

## Gyakori Opciók
- `-n`: A prioritás értékének megadása.
- `-p`: A módosítani kívánt folyamat azonosítója (PID).
- `-g`: Csoport prioritásának módosítása.
- `-u`: Felhasználó által indított folyamat prioritásának módosítása.

## Gyakori Példák
1. A folyamat prioritásának csökkentése:
   ```bash
   renice -n 10 -p 1234
   ```
   Ebben az esetben a 1234 PID-jű folyamat prioritását 10-re állítjuk.

2. A folyamat prioritásának növelése:
   ```bash
   renice -n -5 -p 5678
   ```
   Itt a 5678 PID-jű folyamat prioritását -5-re módosítjuk, ami magasabb prioritást jelent.

3. Csoport prioritásának módosítása:
   ```bash
   renice -n 5 -g 1001
   ```
   Ez a parancs a 1001-es csoporthoz tartozó folyamatok prioritását 5-re állítja.

4. Felhasználó által indított folyamatok prioritásának módosítása:
   ```bash
   renice -n 15 -u username
   ```
   Ezzel a parancssal a megadott felhasználó által indított folyamatok prioritását 15-re állítjuk.

## Tippek
- Mindig ellenőrizd a folyamatok prioritását a `ps` vagy `top` parancsokkal, mielőtt módosítanád azokat.
- A negatív prioritás értékek (pl. -1, -5) magasabb prioritást jelentenek, míg a pozitív értékek (pl. 1, 10) alacsonyabbat.
- Használj `sudo`-t, ha rendszerszintű folyamatok prioritását szeretnéd módosítani, mivel ezekhez magasabb jogosultságok szükségesek.