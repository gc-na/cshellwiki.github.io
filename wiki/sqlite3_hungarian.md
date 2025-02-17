# [Linux] Bash sqlite3 használata: SQLite adatbázisok kezelése

## Áttekintés
Az `sqlite3` parancs egy parancssori eszköz, amely lehetővé teszi az SQLite adatbázisok létrehozását, kezelését és lekérdezését. Az SQLite egy könnyű, beágyazott adatbázis-kezelő rendszer, amely ideális kisebb alkalmazásokhoz és fejlesztési környezetekhez.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
sqlite3 [opciók] [argumentumok]
```

## Gyakori opciók
- `-help`: Megjeleníti a súgót és a parancs használatát.
- `-version`: Megjeleníti az SQLite verzióját.
- `-init <file>`: Inicializál egy adatbázist egy megadott SQL fájl alapján.
- `-batch`: Batch módban futtatja a parancsokat, ami megakadályozza a kimenet interaktív megjelenítését.

## Gyakori példák

1. **Adatbázis létrehozása vagy megnyitása**:
   ```bash
   sqlite3 mydatabase.db
   ```

2. **SQL parancs futtatása egy fájlból**:
   ```bash
   sqlite3 mydatabase.db < script.sql
   ```

3. **Adatok lekérdezése**:
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

4. **Új tábla létrehozása**:
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

5. **Adatok beszúrása**:
   ```bash
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('John Doe');"
   ```

## Tippek
- Mindig készíts biztonsági másolatot az adatbázisokról, mielőtt módosításokat végeznél.
- Használj SQL fájlokat a parancsok tárolására és futtatására, hogy könnyebben kezelhesd a bonyolultabb lekérdezéseket.
- Használj `-batch` opciót, ha automatizált szkriptekben használod az `sqlite3`-at, hogy elkerüld az interaktív kimenetet.