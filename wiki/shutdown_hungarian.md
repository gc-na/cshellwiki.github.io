# [Linux] Bash leállítás használata: A rendszer leállítása vagy újraindítása

## Áttekintés
A `shutdown` parancs a Linux operációs rendszerekben a számítógép leállítására vagy újraindítására szolgál. Ezzel a parancssal biztonságosan lehet leállítani a rendszert, lehetővé téve a felhasználók számára, hogy időben elmenthessék munkájukat.

## Használat
A `shutdown` parancs alapvető szintaxisa a következő:

```bash
shutdown [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: A rendszer leállítása.
- `-r`: A rendszer újraindítása.
- `now`: Azonnali leállítás vagy újraindítás.
- `+m`: A rendszer leállítása vagy újraindítása m perc múlva.
- `hh:mm`: A rendszer leállítása vagy újraindítása egy adott időpontban.

## Gyakori példák
1. A rendszer azonnali leállítása:
    ```bash
    shutdown -h now
    ```

2. A rendszer újraindítása:
    ```bash
    shutdown -r now
    ```

3. A rendszer leállítása 10 perc múlva:
    ```bash
    shutdown -h +10
    ```

4. A rendszer leállítása egy adott időpontban (pl. 15:30):
    ```bash
    shutdown -h 15:30
    ```

5. A leállítás megszakítása (ha már be van állítva):
    ```bash
    shutdown -c
    ```

## Tippek
- Mindig értesítsd a felhasználókat a leállítás előtt, hogy elkerüld az adatvesztést.
- Használj `-r` opciót, ha a rendszer újraindítása szükséges, hogy a frissítések érvénybe lépjenek.
- A `shutdown` parancs használata előtt győződj meg arról, hogy adminisztrátori jogosultságokkal rendelkezel.