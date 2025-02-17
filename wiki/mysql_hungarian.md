# [Linux] Bash mysql használata: Adatbázisok kezelése parancssorból

## Áttekintés
A `mysql` parancs a MySQL adatbázis-kezelő rendszer parancssori interfésze, amely lehetővé teszi az adatbázisok kezelését, lekérdezések végrehajtását és adminisztrációs feladatok elvégzését.

## Használat
A `mysql` parancs alapvető szintaxisa a következő:

```bash
mysql [opciók] [argumentumok]
```

## Gyakori opciók
- `-u, --user`: A felhasználónév megadása az adatbázis eléréséhez.
- `-p, --password`: A jelszó megadása (a jelszó megadásához a parancs futtatása után kérdezi a rendszer).
- `-h, --host`: Az adatbázis szerverének címe (alapértelmezett: localhost).
- `-D, --database`: Az alapértelmezett adatbázis megadása a kapcsolódáskor.
- `-e`: Egyetlen SQL parancs végrehajtása a parancssorból.

## Gyakori példák
1. **Kapcsolódás egy helyi adatbázishoz:**

```bash
mysql -u root -p
```

2. **SQL parancs végrehajtása közvetlenül a parancssorból:**

```bash
mysql -u root -p -e "SHOW DATABASES;"
```

3. **Kapcsolódás egy távoli adatbázishoz:**

```bash
mysql -u felhasználónév -p -h távoli_szerver_címe
```

4. **Adatbázis kiválasztása és táblák listázása:**

```bash
mysql -u root -p -D adatbázis_neve -e "SHOW TABLES;"
```

## Tippek
- Mindig használj erős jelszót az adatbázis felhasználói fiókjához.
- Használj `-D` opciót, hogy közvetlenül egy adott adatbázisra kapcsolódj.
- A `--help` opcióval megtekintheted a `mysql` parancs összes elérhető opcióját.
- Ha gyakran használod a `mysql` parancsot, érdemes lehet alias-t létrehozni a parancs egyszerűsítésére.