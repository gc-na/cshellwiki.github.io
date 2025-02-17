# [Linux] Bash date használata: Dátum és idő megjelenítése

## Áttekintés
A `date` parancs a Linux és Unix rendszerekben a jelenlegi dátum és idő megjelenítésére szolgál. Ezen kívül lehetőséget biztosít a dátumok formázására és manipulálására is.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
date [opciók] [argumentumok]
```

## Gyakori opciók
- `+FORMAT`: A megjelenítési formátum megadása. Például `%Y` az év, `%m` a hónap, `%d` a nap.
- `-u`: Az időzóna UTC (Coordinated Universal Time) szerinti megjelenítése.
- `-d STRING`: Egy adott dátum vagy idő megjelenítése, amelyet a STRING paraméter határoz meg.

## Gyakori példák
1. **Jelenlegi dátum és idő megjelenítése:**
   ```bash
   date
   ```

2. **Dátum formázása:**
   ```bash
   date "+%Y-%m-%d"
   ```

3. **Csak az idő megjelenítése:**
   ```bash
   date "+%H:%M:%S"
   ```

4. **Dátum megadása egy adott időpontban:**
   ```bash
   date -d "2023-10-01"
   ```

5. **UTC idő megjelenítése:**
   ```bash
   date -u
   ```

## Tippek
- Használj formátumokat a `+FORMAT` opcióval, hogy a kívánt megjelenítést kapd.
- A `-d` opcióval könnyen megjelenítheted a jövőbeli vagy múltbeli dátumokat.
- A `date` parancs kimenete scripteléshez is hasznos lehet, például fájlnevek generálásához a dátum alapján.