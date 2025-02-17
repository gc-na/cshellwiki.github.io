# [Linux] Bash if használata: Feltételes végrehajtás

## Overview
Az `if` parancs lehetővé teszi, hogy feltételes logikát alkalmazzunk Bash szkriptekben. Ezzel a parancssal ellenőrizhetjük, hogy egy adott feltétel igaz-e, és ennek megfelelően végrehajthatunk különböző parancsokat.

## Usage
A `if` parancs alapvető szintaxisa a következő:

```bash
if [ feltétel ]; then
    parancsok
fi
```

## Common Options
- `-e`: Ellenőrzi, hogy a megadott fájl létezik-e.
- `-d`: Ellenőrzi, hogy a megadott fájl egy könyvtár-e.
- `-f`: Ellenőrzi, hogy a megadott fájl egy normál fájl-e.
- `-z`: Ellenőrzi, hogy a megadott változó üres-e.
- `-n`: Ellenőrzi, hogy a megadott változó nem üres-e.

## Common Examples

### Példa 1: Fájl létezésének ellenőrzése
```bash
if [ -e "file.txt" ]; then
    echo "A fájl létezik."
else
    echo "A fájl nem létezik."
fi
```

### Példa 2: Változó ellenőrzése
```bash
my_var="Hello"
if [ -n "$my_var" ]; then
    echo "A változó nem üres."
else
    echo "A változó üres."
fi
```

### Példa 3: Könyvtár ellenőrzése
```bash
if [ -d "/path/to/directory" ]; then
    echo "A megadott útvonal egy könyvtár."
else
    echo "A megadott útvonal nem könyvtár."
fi
```

### Példa 4: Több feltétel ellenőrzése
```bash
if [ -f "file.txt" ] && [ -r "file.txt" ]; then
    echo "A fájl létezik és olvasható."
else
    echo "A fájl nem létezik vagy nem olvasható."
fi
```

## Tips
- Mindig használj szóközöket a zárójelek körül, hogy elkerüld a szintaktikai hibákat.
- Használj `elif`-et, ha több feltételt szeretnél ellenőrizni egymás után.
- A `fi` kulcsszóval zárd le az `if` blokkot, hogy a Bash tudja, hol ér véget a feltételes logika.