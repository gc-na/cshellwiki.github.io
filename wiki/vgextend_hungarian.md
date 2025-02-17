# [Linux] Bash vgextend használat: Lépések a logikai kötetek bővítéséhez

## Áttekintés
A `vgextend` parancs a Linux operációs rendszerben a logikai kötetek (LVM) bővítésére szolgál. Ezzel a parancsal új fizikai köteteket adhatunk hozzá egy meglévő logikai kötet csoporthoz, lehetővé téve a tárolókapacitás növelését.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
vgextend [opciók] [logikai_kötet_csoport] [fizikai_kötet]
```

## Gyakori opciók
- `-f`, `--force`: Kényszeríti a parancs végrehajtását, még akkor is, ha az adatok elvesztésével járhat.
- `-n`, `--no-pool`: Megakadályozza a kötetek automatikus bővítését a csoportban.
- `-v`, `--verbose`: Részletes kimenetet ad a végrehajtás során.

## Gyakori példák
1. **Fizikai kötet hozzáadása egy logikai kötet csoporthoz:**
   ```bash
   vgextend myvg /dev/sdb1
   ```

2. **Több fizikai kötet egyidejű hozzáadása:**
   ```bash
   vgextend myvg /dev/sdb1 /dev/sdc1
   ```

3. **Kényszerített bővítés:**
   ```bash
   vgextend -f myvg /dev/sdb1
   ```

4. **Részletes kimenet megjelenítése:**
   ```bash
   vgextend -v myvg /dev/sdb1
   ```

## Tippek
- Mindig ellenőrizze a meglévő logikai kötetek állapotát a `vgdisplay` paranccsal a bővítés előtt.
- Használja a `lvextend` parancsot a logikai kötetek tényleges méretének növeléséhez a `vgextend` után.
- Készítsen biztonsági másolatot az adatokról, mielőtt bármilyen változtatást végezne a köteteken.