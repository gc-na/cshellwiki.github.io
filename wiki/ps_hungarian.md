# [Linux] Bash ps használata: Folyamatok listázása

## Áttekintés
A `ps` parancs a folyamatok állapotának megjelenítésére szolgál a Linux és Unix alapú operációs rendszerekben. Segítségével információkat kaphatunk a futó folyamatokról, például azok azonosítójáról (PID), állapotáról és a felhasználóról, aki elindította őket.

## Használat
A `ps` parancs alapvető szintaxisa a következő:

```bash
ps [opciók] [argumentumok]
```

## Gyakori opciók
- `-e` vagy `-A`: Minden folyamat megjelenítése.
- `-f`: Teljes formátumú megjelenítés, több információval.
- `-u [felhasználónév]`: Csak a megadott felhasználó folyamatait jeleníti meg.
- `-p [PID]`: Csak a megadott azonosítójú folyamatot mutatja.
- `aux`: Az összes folyamat részletes listázása, beleértve a más felhasználók folyamatait is.

## Gyakori példák
1. Minden folyamat megjelenítése:
   ```bash
   ps -e
   ```

2. Folyamatok teljes formátumban:
   ```bash
   ps -ef
   ```

3. Csak egy adott felhasználó folyamatai:
   ```bash
   ps -u username
   ```

4. Egy adott PID-hez tartozó folyamat megjelenítése:
   ```bash
   ps -p 1234
   ```

5. Az összes folyamat részletes listázása:
   ```bash
   ps aux
   ```

## Tippek
- Használja a `ps` parancsot a `grep` parancssal kombinálva, hogy könnyen megtalálja a keresett folyamatokat:
  ```bash
  ps aux | grep firefox
  ```
- A `watch` parancs segítségével folyamatosan figyelheti a folyamatok állapotát:
  ```bash
  watch -n 1 'ps aux'
  ```
- A `ps` parancs kimenete szűrhető és rendezhető a `sort` és `grep` parancsokkal, így könnyen testre szabhatja az információkat.