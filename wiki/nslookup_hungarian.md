# [Linux] Bash nslookup használata: DNS lekérdezések végrehajtása

## Áttekintés
Az `nslookup` parancs egy hálózati eszköz, amely lehetővé teszi a Domain Name System (DNS) lekérdezések végrehajtását. Ezzel a paranccsal IP-címeket kérdezhetünk le domain nevekről, vagy fordítva, domain neveket IP-címekről.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
nslookup [opciók] [argumentumok]
```

## Gyakori Opciók
- `-type=TYPE`: Meghatározza a lekérdezett rekord típusát (pl. A, AAAA, MX).
- `-timeout=SECONDS`: Beállítja a várakozási időt másodpercekben a válaszra.
- `-retry=COUNT`: Beállítja a próbálkozások számát, ha a válasz nem érkezik meg.

## Gyakori Példák
1. **Domain név IP-címének lekérdezése:**
   ```bash
   nslookup example.com
   ```

2. **IP-címhez tartozó domain név lekérdezése:**
   ```bash
   nslookup 93.184.216.34
   ```

3. **Specifikus rekordtípus lekérdezése (pl. MX rekord):**
   ```bash
   nslookup -type=MX example.com
   ```

4. **Egyéni DNS szerver használata:**
   ```bash
   nslookup example.com 8.8.8.8
   ```

## Tippek
- Használja a `-debug` opciót a részletes hibakeresési információk megjelenítéséhez.
- Ellenőrizze a DNS válaszokat különböző DNS szerverek használatával, hogy az esetleges problémákat azonosítani tudja.
- A `nslookup` parancsot gyakran használják a hálózati problémák diagnosztizálására, ezért érdemes ismerni a különböző rekordtípusokat és azok jelentését.