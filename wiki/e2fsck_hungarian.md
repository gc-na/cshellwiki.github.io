# [Linux] Bash e2fsck használata: fájlrendszer ellenőrzése és javítása

## Áttekintés
Az `e2fsck` parancs az ext2, ext3 és ext4 fájlrendszerek ellenőrzésére és javítására szolgál Linux operációs rendszerekben. Ez a parancs segít a fájlrendszer integritásának biztosításában, és képes észlelni és kijavítani a fájlrendszer hibáit.

## Használat
A parancs alapvető szintaxisa a következő:

```
e2fsck [opciók] [argumentumok]
```

## Gyakori opciók
- `-p`: Automatikus javítás, ha lehetséges, anélkül, hogy a felhasználót kérdezné.
- `-f`: Kényszerített ellenőrzés, még akkor is, ha a fájlrendszernek nincs szüksége rá.
- `-n`: Csak olvasási módban fut, nem végez el semmilyen javítást.
- `-y`: Automatikusan igent mond minden kérdésre, így a javítások automatikusan végrehajtódnak.

## Gyakori példák
1. Fájlrendszer ellenőrzése és javítása:
   ```bash
   e2fsck /dev/sda1
   ```

2. Automatikus javítás engedélyezése:
   ```bash
   e2fsck -p /dev/sda1
   ```

3. Kényszerített ellenőrzés végrehajtása:
   ```bash
   e2fsck -f /dev/sda1
   ```

4. Csak olvasási módban történő ellenőrzés:
   ```bash
   e2fsck -n /dev/sda1
   ```

5. Minden kérdésre automatikus válasz igennel:
   ```bash
   e2fsck -y /dev/sda1
   ```

## Tippek
- Mindig készítsen biztonsági másolatot a fontos adatairól, mielőtt fájlrendszer ellenőrzést végezne.
- Használja a `-n` opciót először, hogy megnézze, milyen hibák vannak, anélkül, hogy azonnal javítaná őket.
- A fájlrendszer ellenőrzését a rendszer indítása előtt érdemes elvégezni, hogy elkerülje a fájlok használatát közben.