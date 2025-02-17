# [Linux] Bash lvextend használata: Lemezterület bővítése

## Áttekintés
Az `lvextend` parancs a logikai kötetek (Logical Volume) méretének növelésére szolgál a Linux operációs rendszerekben. Ezzel a parancsal a meglévő logikai kötetekhez további lemezterületet adhatunk hozzá, lehetővé téve a fájlrendszer bővítését.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
lvextend [opciók] [argumentumok]
```

## Gyakori opciók
- `-L, --size`: A logikai kötet új mérete.
- `-l, --extents`: A logikai kötet kiterjedésének (extent) megadása.
- `-r, --resizefs`: A fájlrendszer automatikus bővítése a logikai kötet bővítése után.

## Gyakori példák
1. **Logikai kötet méretének növelése egy adott méretre:**
   ```bash
   lvextend -L +10G /dev/vg0/lv0
   ```
   Ez a parancs 10 GB-tal növeli meg a `/dev/vg0/lv0` logikai kötet méretét.

2. **Logikai kötet kiterjedésének megadása:**
   ```bash
   lvextend -l +100 /dev/vg0/lv0
   ```
   Ezzel a paranccsal 100 kiterjedést (extent) adunk hozzá a logikai kötethez.

3. **Logikai kötet bővítése és fájlrendszer automatikus bővítése:**
   ```bash
   lvextend -r -L +5G /dev/vg0/lv0
   ```
   Ez a parancs 5 GB-tal növeli a logikai kötet méretét, és automatikusan bővíti a fájlrendszert is.

## Tippek
- Mindig ellenőrizze a rendelkezésre álló lemezterületet a bővítés előtt a `vgs` vagy `pvs` parancsokkal.
- A bővítés előtt készítsen biztonsági másolatot az adatokról, hogy elkerülje az esetleges adatvesztést.
- Használja a `-r` opciót, ha szeretné, hogy a fájlrendszer automatikusan bővüljön a logikai kötet bővítésekor, így nem kell külön parancsot futtatnia a fájlrendszer bővítéséhez.