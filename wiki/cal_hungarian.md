# [Linux] Bash cal használata: Naptár megjelenítése

## Áttekintés
A `cal` parancs egy egyszerű eszköz a naptárak megjelenítésére a Bash környezetben. Lehetővé teszi, hogy gyorsan és könnyen megtekintsük a hónapok és évek naptárát.

## Használat
A `cal` parancs alapvető szintaxisa a következő:

```bash
cal [opciók] [argumentumok]
```

## Gyakori opciók
- `-m`: A hónapok neveit rövidítve jeleníti meg.
- `-y`: Az aktuális év naptárát jeleníti meg.
- `-3`: Az aktuális hónapot, az előző hónapot és a következő hónapot mutatja.
- `-1`: Az aktuális hónap naptárát jeleníti meg (ez az alapértelmezett).
- `-A [n]`: A megadott számú hónapot a jövőben mutatja.
- `-B [n]`: A megadott számú hónapot a múltban mutatja.

## Gyakori példák
1. Az aktuális hónap naptárának megjelenítése:
   ```bash
   cal
   ```

2. Egy adott hónap és év naptárának megjelenítése (pl. 2023. november):
   ```bash
   cal 11 2023
   ```

3. Az aktuális év naptárának megjelenítése:
   ```bash
   cal -y
   ```

4. Az aktuális hónap, az előző hónap és a következő hónap megjelenítése:
   ```bash
   cal -3
   ```

5. A következő 3 hónap naptárának megjelenítése:
   ```bash
   cal -A 3
   ```

## Tippek
- Használja a `-m` opciót, ha szeretné, hogy a hónapok nevei rövidítve jelenjenek meg, így helyet takaríthat meg a terminálon.
- A `cal` parancsot kombinálhatja más parancsokkal, például a `grep`-pel, hogy keresést végezzen a naptárban.
- Ne feledje, hogy a `cal` parancs a rendszer időbeállításait használja, így győződjön meg róla, hogy azok helyesek.