# [Linux] Bash tune2fs használata: fájlrendszer paraméterek módosítása

## Áttekintés
A `tune2fs` parancs lehetővé teszi az ext2, ext3 és ext4 fájlrendszerek paramétereinek módosítását. Ezzel a paranccsal beállíthatjuk a fájlrendszer jellemzőit, például a maximális fájlméretet, a naplózási beállításokat és más fontos paramétereket.

## Használat
A `tune2fs` parancs alapvető szintaxisa a következő:

```bash
tune2fs [opciók] [argumentumok]
```

## Gyakori opciók
- `-c <count>`: Beállítja a fájlrendszer maximális csatolási számát.
- `-i <interval>`: Beállítja a fájlrendszer ellenőrzési intervallumát.
- `-m <reserved-blocks>`: Beállítja a fenntartott blokkok arányát.
- `-O <feature>`: Engedélyez egy új fájlrendszer funkciót.
- `-L <label>`: Beállítja a fájlrendszer címkéjét.
- `-e <errors>`: Meghatározza, hogy mi történjen hiba esetén.

## Gyakori példák
1. **Maximális csatolási szám beállítása:**
   ```bash
   tune2fs -c 30 /dev/sda1
   ```

2. **Ellenőrzési intervallum beállítása 6 hónapra:**
   ```bash
   tune2fs -i 6m /dev/sda1
   ```

3. **Fenntartott blokkok arányának módosítása 5%-ra:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Fájlrendszer címkéjének beállítása:**
   ```bash
   tune2fs -L mylabel /dev/sda1
   ```

5. **Új funkció engedélyezése:**
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

## Tippek
- Mindig készítsünk biztonsági másolatot a fájlrendszerről a `tune2fs` parancs használata előtt, mivel a paraméterek módosítása kockázatos lehet.
- Ellenőrizzük a fájlrendszer integritását a `fsck` paranccsal a `tune2fs` használata előtt és után.
- Használjunk `man tune2fs` parancsot a részletes dokumentáció megtekintéséhez és a parancs további lehetőségeinek felfedezéséhez.