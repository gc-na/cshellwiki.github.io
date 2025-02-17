# [Linux] Bash case használat: Kifejezések minták szerint

## Áttekintés
A `case` parancs a Bash-ban lehetővé teszi, hogy egy változó értékét több mintával hasonlítsuk össze. Ez a parancs segít a programozóknak és a rendszergazdáknak a döntéshozatal automatizálásában, lehetővé téve, hogy különböző utasításokat hajtsanak végre a változó értékének megfelelően.

## Használat
A `case` parancs alapvető szintaxisa a következő:

```bash
case [változó] in
    minta1)
        utasítás1
        ;;
    minta2)
        utasítás2
        ;;
    *)
        alapértelmezett_utasítás
        ;;
esac
```

## Gyakori lehetőségek
- `*)`: Az alapértelmezett eset, amely akkor fut le, ha egyik minta sem egyezik.
- `;;`: A blokk végét jelzi, amely megmutatja, hogy a következő minta ellenőrzése következik.

## Gyakori példák

### 1. Egyszerű példa
Egy változó értékének ellenőrzése és a megfelelő üzenet kiírása:

```bash
read -p "Kérem, adja meg a nap nevét: " nap
case $nap in
    hétfő)
        echo "Ma hétfő van."
        ;;
    kedd)
        echo "Ma kedd van."
        ;;
    szerda)
        echo "Ma szerda van."
        ;;
    *)
        echo "Ez nem egy hétköznap."
        ;;
esac
```

### 2. Számok ellenőrzése
Számok osztályozása:

```bash
read -p "Kérem, adjon meg egy számot: " szam
case $szam in
    1|2|3)
        echo "Az szám 1, 2 vagy 3."
        ;;
    4|5|6)
        echo "Az szám 4, 5 vagy 6."
        ;;
    *)
        echo "Az szám nem 1, 2, 3, 4, 5 vagy 6."
        ;;
esac
```

### 3. Fájl kiterjesztések kezelése
Fájlok kiterjesztéseinek ellenőrzése:

```bash
read -p "Kérem, adjon meg egy fájlnevet: " fajl
case $fajl in
    *.txt)
        echo "Ez egy szövegfájl."
        ;;
    *.jpg|*.png)
        echo "Ez egy kép fájl."
        ;;
    *)
        echo "Ismeretlen fájl típus."
        ;;
esac
```

## Tippek
- Mindig használj `;;` jelet a minták végén, hogy elkerüld a nem kívánt viselkedést.
- Használj `*)` mintát az alapértelmezett esethez, hogy kezelni tudd az ismeretlen bemeneteket.
- A `case` parancs használata tisztábbá és olvashatóbbá teszi a kódot, különösen, ha sok feltételt kell kezelni.