# [Linux] Bash fsck használata: Fájl rendszer ellenőrzése és javítása

## Áttekintés
Az `fsck` (file system check) parancs a fájlrendszerek ellenőrzésére és javítására szolgál. Ez a parancs segít azonosítani és kijavítani a fájlrendszerben előforduló hibákat, biztosítva ezzel a rendszer stabilitását és integritását.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
fsck [opciók] [argumentumok]
```

## Gyakori Opciók
- `-a` vagy `--auto`: Automatikusan javítja a hibákat, anélkül, hogy megerősítést kérne.
- `-n` vagy `--no`: Csak ellenőrzi a fájlrendszert, javítás nélkül.
- `-y`: Automatikusan igent mond minden javításra.
- `-t`: Megadja, hogy melyik fájlrendszert ellenőrizzük (pl. ext4, xfs).

## Gyakori Példák
1. Fájl rendszer ellenőrzése automatikus javítással:
   ```bash
   fsck -a /dev/sda1
   ```

2. Fájl rendszer ellenőrzése megerősítés nélkül:
   ```bash
   fsck -n /dev/sda2
   ```

3. Minden fájlrendszer ellenőrzése a rendszerindításkor:
   ```bash
   fsck -A
   ```

4. Fájl rendszer ellenőrzése és minden javítás automatikus elfogadása:
   ```bash
   fsck -y /dev/sda3
   ```

## Tippek
- Mindig készítsen biztonsági másolatot a fontos adatokról a fájlrendszer ellenőrzése előtt.
- Használja a `-n` opciót, ha először csak ellenőrizni szeretné a fájlrendszert anélkül, hogy bármilyen változtatást végezne.
- A `fsck` parancsot legjobb, ha a fájlrendszer nem aktív állapotában futtatja, például a rendszerindítás során vagy egy live CD-ről.