# [Linux] Bash psql használata: PostgreSQL adatbázisok kezelése

## Áttekintés
A `psql` parancs a PostgreSQL adatbázis-kezelő rendszer parancssori felülete. Lehetővé teszi az adatbázisok kezelését, lekérdezések futtatását és az adatbázisokkal kapcsolatos műveletek végrehajtását.

## Használat
A `psql` parancs alapvető szintaxisa a következő:

```bash
psql [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Az adatbázis szerverének címe.
- `-p`: Az adatbázis portja.
- `-U`: Az adatbázis felhasználóneve.
- `-d`: Az adatbázis neve, amelyhez csatlakozni szeretnénk.
- `-f`: SQL fájl futtatása.

## Gyakori példák
1. **Kapcsolódás egy adatbázishoz**:
   ```bash
   psql -U felhasználónév -d adatbázisnév
   ```

2. **SQL parancs futtatása fájlból**:
   ```bash
   psql -U felhasználónév -d adatbázisnév -f parancsok.sql
   ```

3. **Adatbázis listázása**:
   ```bash
   psql -U felhasználónév -d adatbázisnév -c "\l"
   ```

4. **Tábla létrehozása**:
   ```bash
   psql -U felhasználónév -d adatbázisnév -c "CREATE TABLE pelda (id SERIAL PRIMARY KEY, nev VARCHAR(100));"
   ```

5. **Adatok lekérdezése**:
   ```bash
   psql -U felhasználónév -d adatbázisnév -c "SELECT * FROM pelda;"
   ```

## Tippek
- Mindig használj erős jelszót az adatbázis felhasználóknál.
- Használj SQL fájlokat a bonyolultabb lekérdezésekhez, hogy könnyebben kezelhesd őket.
- A `\?` parancsot használva megtekintheted a `psql` parancs összes elérhető parancsát és opcióját.