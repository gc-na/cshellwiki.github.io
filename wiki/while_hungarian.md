# [Linux] Bash while használata: Ciklusok végrehajtása

## Áttekintés
A `while` parancs egy ciklusvezérlő szerkezet a Bash-ban, amely lehetővé teszi, hogy egy adott parancsot vagy parancsok sorozatát addig hajtsuk végre, amíg egy megadott feltétel igaz. Ez hasznos lehet, ha ismétlődő feladatokat kell végrehajtani, amíg egy bizonyos állapot el nem érkezik.

## Használat
A `while` parancs alapvető szintaxisa a következő:

```bash
while [feltétel]
do
    [parancsok]
done
```

## Gyakori opciók
A `while` parancsnak nincsenek specifikus opciói, mivel a működése a megadott feltételtől függ. Azonban a feltételek és parancsok formázása során használhatók általános Bash opciók, mint például:
- `-n`: Ellenőrzi, hogy a megadott karakterlánc nem üres.
- `-z`: Ellenőrzi, hogy a megadott karakterlánc üres.

## Gyakori példák

### Példa 1: Számláló ciklus
Ez a példa egy egyszerű számlálót valósít meg, amely 1-től 5-ig számol.

```bash
count=1
while [ $count -le 5 ]
do
    echo "Számláló: $count"
    ((count++))
done
```

### Példa 2: Felhasználói bemenet
Ez a példa folyamatosan kéri a felhasználótól a bemenetet, amíg az "exit" szót nem írja be.

```bash
input=""
while [ "$input" != "exit" ]
do
    read -p "Írj be valamit (exit a kilépéshez): " input
    echo "Beírtad: $input"
done
```

### Példa 3: Fájlok feldolgozása
Ez a példa végigiterál egy könyvtár összes fájlján, és kiírja a nevüket.

```bash
files=$(ls)
while [ ! -z "$files" ]
do
    echo "Fájl: $files"
    files=$(ls | tail -n +2) # Az első fájl eltávolítása a listából
done
```

## Tippek
- Mindig ellenőrizd a ciklus feltételeit, hogy elkerüld az infini ciklusokat.
- Használj `break` parancsot a ciklus megszakításához, ha egy bizonyos feltétel teljesül.
- A `sleep` parancs használata hasznos lehet, ha a ciklus túl gyorsan fut, és szeretnéd csökkenteni a CPU terhelést.