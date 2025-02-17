# [Linux] Bash crontab használata: Ütemezett feladatok kezelése

## Áttekintés
A `crontab` parancs lehetővé teszi ütemezett feladatok (cron jobok) létrehozását és kezelését a Unix-alapú rendszereken. Ezzel a parancssal automatikusan futtathatunk parancsokat vagy szkripteket meghatározott időpontokban vagy időközönként.

## Használat
A `crontab` parancs alapvető szintaxisa a következő:

```
crontab [opciók] [argumentumok]
```

## Gyakori opciók
- `-e`: A felhasználó crontab fájljának szerkesztése.
- `-l`: A felhasználó crontab fájljának megjelenítése.
- `-r`: A felhasználó crontab fájljának törlése.
- `-i`: Megerősítést kér a törlés előtt.

## Gyakori példák
1. **Crontab fájl szerkesztése:**
   ```bash
   crontab -e
   ```
   Ezzel a paranccsal megnyitjuk a felhasználó crontab fájlját szerkesztésre.

2. **Crontab fájl megjelenítése:**
   ```bash
   crontab -l
   ```
   Ezzel a paranccsal megtekinthetjük a jelenlegi ütemezett feladatainkat.

3. **Crontab fájl törlése:**
   ```bash
   crontab -r
   ```
   Ez a parancs törli a felhasználó crontab fájlját. (Figyelem: az `-i` opcióval megerősítést kérhet a törlés előtt.)

4. **Feladat ütemezése:**
   ```bash
   * * * * * /path/to/script.sh
   ```
   Ez a példa minden percben futtatja a `script.sh` szkriptet.

5. **Napi feladat ütemezése:**
   ```bash
   0 2 * * * /path/to/backup.sh
   ```
   Ezzel a paranccsal a `backup.sh` szkript minden nap 2:00-kor fut le.

## Tippek
- Mindig ellenőrizd a crontab fájl szintaxisát, hogy elkerüld a hibákat.
- Használj abszolút elérési utakat a szkriptekhez, hogy biztosan megtalálja őket a cron.
- A cron kimenete alapértelmezés szerint nem jelenik meg a terminálban, érdemes kimenetet naplózni egy fájlba, például: `* * * * * /path/to/script.sh >> /path/to/logfile.log 2>&1`.
- Ne felejtsd el, hogy a cron környezete eltérhet a felhasználói környezettől, így lehet, hogy a környezeti változókat explicit módon kell beállítani.