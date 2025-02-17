# [Linux] Bash lvs használata: Logikai kötetek megjelenítése

## Áttekintés
Az `lvs` parancs a LVM (Logical Volume Manager) eszközkészlet része, amely lehetővé teszi a logikai kötetek listázását és megjelenítését. Ezzel a paranccsal könnyen áttekinthetjük a rendszerünkben található logikai köteteket, azok méretét és állapotát.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
lvs [opciók] [érvek]
```

## Gyakori opciók
- `-o`: Megadja, hogy mely oszlopokat szeretnénk megjeleníteni.
- `--units`: Meghatározza az egységeket, amelyekben a méreteket szeretnénk látni (pl. kB, MB, GB).
- `-a`: Minden logikai kötetet megjelenít, beleértve a nem aktívakat is.

## Gyakori példák
1. **Alap logikai kötetek listázása:**
   ```bash
   lvs
   ```

2. **Speciális oszlopok megjelenítése:**
   ```bash
   lvs -o +devices
   ```

3. **Logikai kötetek megjelenítése GB egységekben:**
   ```bash
   lvs --units g
   ```

4. **Minden logikai kötet megjelenítése, beleértve a nem aktívakat is:**
   ```bash
   lvs -a
   ```

## Tippek
- Használj `man lvs` parancsot a részletes dokumentáció megtekintéséhez.
- Kombináld az `lvs` parancsot más LVM parancsokkal, mint például `lvcreate` vagy `lvremove`, a hatékonyabb kötetkezelés érdekében.
- Rendszeresen ellenőrizd a logikai kötetek állapotát, hogy elkerüld a potenciális problémákat.