# [Linux] Bash teszt használata: Feltételek ellenőrzése

## Áttekintés
A `test` parancs a Bash környezetben lehetővé teszi különböző feltételek ellenőrzését, például fájlok létezését, típusát, vagy változók értékét. A `test` parancsot gyakran használják scriptelés során, hogy logikai döntéseket hozzanak.

## Használat
A `test` parancs alapvető szintaxisa a következő:

```bash
test [opciók] [argumentumok]
```

## Gyakori opciók
- `-e`: Ellenőrzi, hogy a megadott fájl létezik-e.
- `-f`: Ellenőrzi, hogy a megadott fájl egy normál fájl-e.
- `-d`: Ellenőrzi, hogy a megadott fájl egy könyvtár-e.
- `-z`: Ellenőrzi, hogy a megadott változó üres-e.
- `=`: Ellenőrzi, hogy két változó értéke megegyezik-e.

## Gyakori példák
1. Fájl létezésének ellenőrzése:
   ```bash
   test -e myfile.txt && echo "A fájl létezik."
   ```

2. Fájl típusának ellenőrzése:
   ```bash
   test -f myfile.txt && echo "Ez egy normál fájl."
   ```

3. Könyvtár ellenőrzése:
   ```bash
   test -d mydirectory && echo "Ez egy könyvtár."
   ```

4. Változó ürességének ellenőrzése:
   ```bash
   myvar=""
   test -z "$myvar" && echo "A változó üres."
   ```

5. Két változó összehasonlítása:
   ```bash
   var1="hello"
   var2="hello"
   test "$var1" = "$var2" && echo "A két változó megegyezik."
   ```

## Tippek
- Használj zárójeleket a `test` parancs helyett, például `[[ ... ]]`, ha Bash környezetben dolgozol, mivel ez több funkciót és jobb hibakezelést kínál.
- A `test` parancsot gyakran használják `if` utasításokban, hogy logikai döntéseket hozzanak a scriptben.
- Mindig idézőjelek között használd a változókat, hogy elkerüld a hibákat, különösen, ha a változók üresek lehetnek.