# [Linux] Bash dig használata: DNS lekérdezések végrehajtása

## Áttekintés
A `dig` (Domain Information Groper) egy parancssori eszköz, amelyet DNS (Domain Name System) lekérdezések végrehajtására használnak. Segítségével információkat nyerhetünk ki domain nevekről, IP címekről és más DNS rekordokról.

## Használat
A `dig` parancs alapvető szintaxisa a következő:

```
dig [opciók] [argumentumok]
```

## Gyakori opciók
- `@server`: Meghatározza a DNS szervert, amelyet a lekérdezéshez használni szeretnénk.
- `-t type`: Megadja a lekérdezni kívánt rekord típusát (pl. A, AAAA, MX).
- `+short`: Csak a rövid választ adja vissza, a részletes információk helyett.

## Gyakori példák
1. **Alapértelmezett A rekord lekérdezés:**
   ```
   dig example.com
   ```

2. **Specifikus DNS szerver használata:**
   ```
   dig @8.8.8.8 example.com
   ```

3. **MX rekord lekérdezés:**
   ```
   dig -t MX example.com
   ```

4. **Rövid válasz megjelenítése:**
   ```
   dig +short example.com
   ```

5. **AAAA rekord lekérdezés IPv6 címhez:**
   ```
   dig -t AAAA example.com
   ```

## Tippek
- Használja a `+trace` opciót a DNS lekérdezések lépésről lépésre történő nyomon követéséhez.
- A `+noall +answer` opciók kombinációja hasznos lehet, ha csak a válaszokat szeretné látni, a többi információ nélkül.
- Érdemes megismerni a különböző rekordtípusokat, hogy a megfelelő információkat tudja lekérdezni.