# [Linux] Bash traceroute használata: Hálózati útvonalak nyomozása

## Áttekintés
A `traceroute` parancs a hálózati forgalom útvonalának nyomozására szolgál. Megmutatja, hogy a csomagok milyen lépéseken keresztül jutnak el a célállomásig, és információt ad a köztes routerekről.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
traceroute [opciók] [cél]
```

## Gyakori opciók
- `-m <max_hop>`: Beállítja a maximális ugrások számát.
- `-n`: Az IP-címek megjelenítése névfeloldás nélkül.
- `-w <másodperc>`: A válaszidő várakozási ideje másodpercben.
- `-p <port>`: A célport megadása, alapértelmezett a 33434.

## Gyakori példák
1. Alap traceroute egy weboldalhoz:
    ```bash
    traceroute www.example.com
    ```

2. Traceroute névfeloldás nélkül:
    ```bash
    traceroute -n www.example.com
    ```

3. Maximális ugrások számának beállítása:
    ```bash
    traceroute -m 15 www.example.com
    ```

4. Válaszidő várakozásának beállítása:
    ```bash
    traceroute -w 2 www.example.com
    ```

5. Célport megadása:
    ```bash
    traceroute -p 80 www.example.com
    ```

## Tippek
- Használj `-n` opciót, ha gyorsabb eredményre van szükséged, és nem fontos a névfeloldás.
- A `traceroute` parancs kimenete segíthet az internetkapcsolati problémák diagnosztizálásában, figyeld a magas késleltetési időt vagy az időtúllépéseket.
- Próbáld ki különböző célpontokkal, hogy megértsd a hálózati struktúrát és a forgalmi mintákat.