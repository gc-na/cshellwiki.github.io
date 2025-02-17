# [Linux] Bash else használat: Feltételes utasítások kezelése

## Áttekintés
Az `else` parancs a Bash szkriptekben használatos, hogy lehetővé tegye a feltételes utasítások végrehajtását. Ha a megadott feltétel nem teljesül, az `else` blokkban található utasítások végrehajtásra kerülnek.

## Használat
Az `else` parancs szintaxisa a következő:

```bash
if [ feltétel ]; then
    # utasítások, ha a feltétel igaz
else
    # utasítások, ha a feltétel hamis
fi
```

## Gyakori opciók
Az `else` parancsnak nincsenek közvetlen opciói, mivel ez egy vezérlési szerkezet. Azonban az `if` parancs használatakor a következő opciókat használhatjuk:

- `-e`: Ellenőrzi, hogy a fájl létezik-e.
- `-d`: Ellenőrzi, hogy a megadott útvonal egy könyvtár-e.
- `-f`: Ellenőrzi, hogy a megadott útvonal egy fájl-e.

## Gyakori példák

### Példa 1: Fájl létezésének ellenőrzése
```bash
if [ -e "file.txt" ]; then
    echo "A fájl létezik."
else
    echo "A fájl nem létezik."
fi
```

### Példa 2: Könyvtár ellenőrzése
```bash
if [ -d "my_directory" ]; then
    echo "A könyvtár létezik."
else
    echo "A könyvtár nem létezik."
fi
```

### Példa 3: Számok összehasonlítása
```bash
number=10
if [ $number -gt 5 ]; then
    echo "A szám nagyobb, mint 5."
else
    echo "A szám nem nagyobb, mint 5."
fi
```

## Tippek
- Mindig zárd le az `if` blokkot `fi`-val, hogy elkerüld a szintaktikai hibákat.
- Használj megfelelő szóközöket a feltételek körül, hogy a Bash helyesen értelmezze őket.
- Az `else` blokk használata segít a program logikájának tisztábbá tételében, így könnyebben átlátható és karbantartható lesz a kódod.