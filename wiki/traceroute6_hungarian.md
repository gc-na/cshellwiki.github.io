# [Linux] Bash traceroute6 használata: IPv6 címek nyomkövetése

## Áttekintés
A `traceroute6` parancs az IPv6 hálózati címek nyomkövetésére szolgál. Segítségével megállapíthatjuk, hogy az adatcsomagok milyen útvonalon haladnak át a hálózaton, és hol találkozhatunk esetleges problémákkal.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
traceroute6 [opciók] [cím]
```

## Gyakori opciók
- `-m <max_hop>`: Beállítja a maximális ugrások számát.
- `-p <port>`: Megadja a port számát, amelyet a traceroute használ.
- `-w <timeout>`: Beállítja a válaszidő időkorlátját másodpercekben.

## Gyakori példák
1. Alap traceroute6 használat egy IPv6 címhez:
   ```bash
   traceroute6 google.com
   ```

2. Maximális ugrások számának beállítása 15-re:
   ```bash
   traceroute6 -m 15 google.com
   ```

3. Port szám megadása 80-ra:
   ```bash
   traceroute6 -p 80 google.com
   ```

4. Válaszidő időkorlát beállítása 2 másodpercre:
   ```bash
   traceroute6 -w 2 google.com
   ```

## Tippek
- Használj `sudo`-t, ha a parancs nem működik megfelelően, mivel bizonyos rendszerek adminisztrátori jogosultságokat igényelnek.
- Ellenőrizd a tűzfal beállításait, mivel ezek befolyásolhatják a traceroute6 működését.
- A traceroute6 kimenete segíthet a hálózati problémák diagnosztizálásában, figyeld meg a válaszidőket és az esetleges időtúllépéseket.