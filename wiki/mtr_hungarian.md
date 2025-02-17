# [Linux] Bash mtr használata: Hálózati útvonalak nyomkövetése

## Áttekintés
Az `mtr` (My Traceroute) egy hálózati diagnosztikai eszköz, amely kombinálja a traceroute és a ping parancsok funkcióit. Segítségével nyomon követhetjük a hálózati csomagok útját egy adott célállomásig, és információt nyerhetünk a hálózati kapcsolat minőségéről.

## Használat
A `mtr` parancs alapvető szintaxisa a következő:

```bash
mtr [opciók] [cél]
```

## Gyakori opciók
- `-r`: Jelentés generálása, amelyet fájlba lehet menteni.
- `-c <szám>`: Megadja, hogy hány ping kérést küldjön.
- `-i <másodperc>`: Beállítja a ping kérések közötti időtartamot.
- `-p`: A port számának megadása, ha a cél szolgáltatás portja eltér a standardtól.

## Gyakori példák
1. Alapértelmezett mtr használat:
   ```bash
   mtr google.com
   ```

2. 10 ping kérés küldése:
   ```bash
   mtr -c 10 google.com
   ```

3. Jelentés generálása fájlba:
   ```bash
   mtr -r -c 5 google.com > mtr_report.txt
   ```

4. Ping kérések közötti idő beállítása 2 másodpercre:
   ```bash
   mtr -i 2 google.com
   ```

## Tippek
- Használj root jogosultságokat az `mtr` futtatásához, hogy a legpontosabb adatokat kapd.
- A `-r` opcióval generált jelentések hasznosak lehetnek a hálózati problémák elemzésében.
- Figyeld a válaszidőket és a csomagvesztéseket, mivel ezek fontos mutatók a hálózati teljesítmény szempontjából.