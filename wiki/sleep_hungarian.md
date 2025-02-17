# [Linux] Bash sleep használat: A parancs késleltetése

## Áttekintés
A `sleep` parancs egy egyszerű eszköz a Bash környezetben, amely lehetővé teszi, hogy a parancssor végrehajtása közben egy meghatározott ideig szüneteltessük a folyamatot. Ez hasznos lehet, ha időzítéseket vagy késleltetett műveleteket szeretnénk végrehajtani.

## Használat
A `sleep` parancs alapvető szintaxisa a következő:

```bash
sleep [opciók] [idő]
```

## Gyakori opciók
- `-h`, `--help`: Megjeleníti a parancs használati útmutatóját.
- `-V`, `--version`: Megjeleníti a verzióinformációt.

## Gyakori példák
1. **Alapvető késleltetés 5 másodpercre:**
   ```bash
   sleep 5
   ```
   Ez a parancs 5 másodpercre megállítja a parancssor végrehajtását.

2. **Késleltetés 2 percig:**
   ```bash
   sleep 2m
   ```
   Itt a `m` jelzi, hogy a késleltetés percekben van megadva.

3. **Késleltetés 1 órára:**
   ```bash
   sleep 1h
   ```
   A `h` opcióval 1 órás késleltetést állíthatunk be.

4. **Késleltetés 10 másodperc és 500 milliszekundum:**
   ```bash
   sleep 10.5
   ```
   Ez a parancs 10,5 másodperces késleltetést hajt végre.

## Tippek
- Használja a `sleep` parancsot szkriptekben, hogy időzítse a különböző parancsok végrehajtását, például várakozva egy háttérfolyamat befejezésére.
- Kísérletezzen a különböző időegységekkel (másodperc, perc, óra), hogy a legjobban illeszkedjen a feladatához.
- Ne feledje, hogy a `sleep` parancs nem megszakítható, így ha egy hosszabb késleltetést állít be, az várakozás alatt nem tud más parancsokat végrehajtani.