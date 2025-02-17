# [Linux] Bash lvcreate használata: Lépésről lépésre logikai kötetek létrehozása

## Áttekintés
Az `lvcreate` parancs a Linux Logical Volume Manager (LVM) eszköze, amely lehetővé teszi logikai kötetek létrehozását. Ezzel a paranccsal új logikai köteteket hozhatunk létre a meglévő fizikai kötetekből, amelyeket később fájlrendszerek tárolására használhatunk.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
lvcreate [opciók] [argumentumok]
```

## Gyakori opciók
- `-n, --name <név>`: A létrehozandó logikai kötet neve.
- `-L, --size <méret>`: A logikai kötet mérete, például `10G` (10 gigabájt).
- `-l, --extents <kiterjedések>`: A logikai kötet méretének megadása kiterjedésekben.
- `-C, --mirrors <tükör>`: Tükör logikai kötet létrehozása.
- `-Z, --zero n` : A kötet inicializálásának beállítása.

## Gyakori példák
1. **Egyszerű logikai kötet létrehozása:**
   ```bash
   lvcreate -n myvolume -L 10G myvg
   ```
   Ez a parancs létrehoz egy `myvolume` nevű, 10 GB méretű logikai kötetet a `myvg` nevű csoportban.

2. **Logikai kötet létrehozása kiterjedések alapján:**
   ```bash
   lvcreate -n myvolume -l 100 myvg
   ```
   Itt a `myvolume` logikai kötet 100 kiterjedésből áll, a `myvg` csoportban.

3. **Tükör logikai kötet létrehozása:**
   ```bash
   lvcreate -n mymirror -L 20G -m 1 myvg
   ```
   Ez a parancs létrehoz egy 20 GB méretű tükör logikai kötetet `mymirror` néven.

## Tippek
- Mindig ellenőrizze a meglévő fizikai köteteket és logikai kötet csoportokat az `lvdisplay` és `pvdisplay` parancsokkal, mielőtt új kötetet hozna létre.
- Használjon megfelelő méretet és nevet a logikai köteteknél, hogy később könnyen azonosíthatóak legyenek.
- Tartsuk szem előtt a lemezterület kihasználtságát, és ne hozzunk létre túl sok kis logikai kötetet, mert ez bonyolíthatja a rendszert.