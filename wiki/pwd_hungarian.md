# [Linux] Bash pwd használat: Az aktuális könyvtár megjelenítése

## Áttekintés
A `pwd` (print working directory) parancs megjeleníti az aktuális munkakönyvtár teljes elérési útját a parancssorban. Ez hasznos lehet, ha szeretnénk tudni, hogy melyik könyvtárban dolgozunk éppen.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
pwd [opciók] [argumentumok]
```

## Gyakori opciók
- `-P`: A fizikai elérési utat mutatja, figyelmen kívül hagyva a szimbolikus linkeket.
- `-L`: A logikai elérési utat mutatja, beleértve a szimbolikus linkeket is (ez az alapértelmezett viselkedés).

## Gyakori példák
1. Az aktuális könyvtár megjelenítése:
   ```bash
   pwd
   ```

2. A fizikai elérési út megjelenítése:
   ```bash
   pwd -P
   ```

3. A logikai elérési út megjelenítése (az alapértelmezett):
   ```bash
   pwd -L
   ```

## Tippek
- Használj `pwd`-t, amikor navigálsz a fájlrendszerben, hogy mindig tudd, hol vagy.
- A `pwd` parancsot gyakran használják más parancsokkal együtt, például szkriptekben, hogy dinamikusan hivatkozzanak az aktuális könyvtárra.
- Ha szimbolikus linkekkel dolgozol, érdemes a `-P` opciót használni, hogy a tényleges könyvtárat lásd.