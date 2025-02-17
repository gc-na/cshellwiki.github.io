# [Linux] Bash hostname használata: A gép neve

## Áttekintés
A `hostname` parancs a számítógép vagy a szerver nevét jeleníti meg vagy állítja be. Ez a név azonosítja a gépet a hálózaton, és fontos szerepet játszik a hálózati kommunikációban.

## Használat
A `hostname` parancs alapvető szintaxisa a következő:

```bash
hostname [opciók] [argumentumok]
```

## Gyakori opciók
- `-f`, `--fqdn`: A teljesen minősített domain nevet (FQDN) jeleníti meg.
- `-i`, `--ip-address`: A gép IP-címét mutatja meg.
- `-s`, `--short`: Csak a rövid gépnevet adja vissza.
- `-d`, `--domain`: A gép domain nevét jeleníti meg.

## Gyakori példák
1. A gép névének megjelenítése:
   ```bash
   hostname
   ```

2. A teljesen minősített domain név megjelenítése:
   ```bash
   hostname -f
   ```

3. A gép IP-címének megjelenítése:
   ```bash
   hostname -i
   ```

4. Csak a rövid gépnév megjelenítése:
   ```bash
   hostname -s
   ```

5. A gép domain nevének megjelenítése:
   ```bash
   hostname -d
   ```

## Tippek
- A `hostname` parancs használata előtt érdemes adminisztrátori jogosultságokkal rendelkezni, ha a gép nevét szeretnéd megváltoztatni.
- A `hostname` beállítása után érdemes újraindítani a hálózati szolgáltatásokat, hogy a változások érvénybe lépjenek.
- A `hostname` parancsot gyakran használják scriptelés során, hogy dinamikusan lekérdezzék a gép nevét.