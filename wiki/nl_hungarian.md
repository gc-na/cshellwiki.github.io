# [Linux] Bash nl használata: fájlok sorszámozása

## Áttekintés
A `nl` parancs a szöveges fájlok sorainak sorszámozására szolgál. Hasznos lehet, ha szeretnénk nyomon követni a sorok számát egy fájlban, vagy ha egy dokumentumot szeretnénk könnyebben olvashatóvá tenni.

## Használat
A `nl` parancs alapvető szintaxisa a következő:

```bash
nl [opciók] [argumentumok]
```

## Gyakori opciók
- `-b`: Meghatározza a sorszámozás típusát (pl. `a` - minden sor, `t` - csak a nem üres sorok).
- `-f`: Megadja, hogy a fájlokban a sorszámozás újrainduljon egy új blokk kezdetén.
- `-n`: Meghatározza a sorszámozás formátumát (pl. `ln` - balra igazított, `rn` - jobbra igazított).
- `-w`: Beállítja a sorszámok szélességét.

## Gyakori példák
1. **Alap sorszámozás**:
   ```bash
   nl myfile.txt
   ```
   Ez a parancs sorszámozza a `myfile.txt` fájl sorait.

2. **Csak a nem üres sorok sorszámozása**:
   ```bash
   nl -b t myfile.txt
   ```
   Itt a `-b t` opcióval csak a nem üres sorokat számozzuk.

3. **Sorszámok formázása**:
   ```bash
   nl -n rn myfile.txt
   ```
   Ez a parancs jobbra igazítja a sorszámokat a fájlban.

4. **Sorszámozás új blokk kezdetén**:
   ```bash
   nl -f myfile.txt
   ```
   A sorszámozás újraindul, amikor egy új blokk kezdődik.

## Tippek
- Használj `man nl` parancsot a `nl` parancs részletes dokumentációjának megtekintéséhez.
- Kísérletezz a különböző opciókkal, hogy megtaláld a legjobban megfelelő formátumot a fájljaidhoz.
- A `nl` parancs kimenetét átirányíthatod egy új fájlba, például: `nl myfile.txt > numbered_file.txt`.