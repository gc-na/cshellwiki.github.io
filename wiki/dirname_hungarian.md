# [Linux] Bash dirname használata: A fájlok elérési útjának kinyerése

## Áttekintés
A `dirname` parancs a megadott fájl elérési útjának könyvtár részét adja vissza. Ez hasznos lehet, ha szeretnénk megtudni, hogy egy fájl melyik könyvtárban található anélkül, hogy a fájl nevét is meg kellene adnunk.

## Használat
A `dirname` parancs alapvető szintaxisa a következő:

```bash
dirname [opciók] [argumentumok]
```

## Gyakori Opciók
- Nincsenek specifikus opciók a `dirname` parancsnál, mivel ez egy egyszerű parancs, amely csak a megadott argumentumot dolgozza fel.

## Gyakori Példák
1. **Egyszerű használat**: A fájl elérési útjának kinyerése.
   ```bash
   dirname /home/felhasználó/dokumentumok/fájl.txt
   ```
   Kimenet:
   ```
   /home/felhasználó/dokumentumok
   ```

2. **Több fájl kezelése**: Több fájl elérési útjának kinyerése.
   ```bash
   dirname /etc/hosts /usr/local/bin/script.sh
   ```
   Kimenet:
   ```
   /etc
   /usr/local/bin
   ```

3. **Relatív elérési út**: Relatív elérési út használata.
   ```bash
   dirname ./fájlok/példa.txt
   ```
   Kimenet:
   ```
   ./fájlok
   ```

## Tippek
- Használja a `dirname` parancsot más parancsokkal kombinálva, például a `find` vagy a `xargs` parancsokkal, hogy dinamikusan kinyerje a fájlok elérési útját.
- A `dirname` parancsot gyakran használják scriptelés során, hogy a fájlok helyét könnyen kezelni tudják.
- Ne feledje, hogy a `dirname` csak a megadott fájlok könyvtárát adja vissza, a fájlneveket nem tartalmazza.