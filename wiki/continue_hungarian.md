# [Linux] Bash continue használata: A ciklus folytatása

## Áttekintés
A `continue` parancs a Bash szkriptekben és parancsokban használatos, hogy a ciklusokban (például `for`, `while`, `until`) a jelenlegi iterációt átugorja, és a következő iterációra lépjen. Ez hasznos lehet, ha bizonyos feltételek mellett nem szeretnénk végrehajtani a ciklus aktuális lépését.

## Használat
A `continue` parancs alapvető szintaxisa a következő:

```bash
continue [n]
```

Ahol az `n` az iterációk számát jelöli, amelyet át szeretnénk ugrani. Ha nem adunk meg értéket, akkor az aktuális ciklus következő iterációjára lép.

## Gyakori opciók
- `n`: Megadja, hogy hány iterációt kell átugrani a ciklusban. Alapértelmezés szerint 1, ha nem adunk meg értéket.

## Gyakori példák

1. **Egyszerű példa a `for` ciklusra:**
   ```bash
   for i in {1..5}; do
       if [ $i -eq 3 ]; then
           continue
       fi
       echo "Szám: $i"
   done
   ```
   *Ez a példa kiírja a számokat 1-től 5-ig, de a 3-as számot kihagyja.*

2. **`while` ciklus használata:**
   ```bash
   count=1
   while [ $count -le 5 ]; do
       if [ $count -eq 4 ]; then
           ((count++))
           continue
       fi
       echo "Számláló: $count"
       ((count++))
   done
   ```
   *Ez a példa a 4-es számot kihagyja, és a többi számot kiírja.*

3. **Bonyolultabb feltétel:**
   ```bash
   for i in {1..10}; do
       if [ $((i % 2)) -eq 0 ]; then
           continue
       fi
       echo "Páratlan szám: $i"
   done
   ```
   *Ez a példa csak a páratlan számokat írja ki 1-től 10-ig.*

## Tippek
- Használj `continue`-t, ha szeretnéd elkerülni a felesleges kód végrehajtását egy ciklusban, ezzel javítva a teljesítményt.
- Mindig ellenőrizd, hogy a `continue` parancs használata nem okoz-e végtelen ciklust, ha nem megfelelően van beállítva a ciklus feltétele.
- A `continue` parancsot kombinálhatod más vezérlési struktúrákkal, mint például `if`-ek, hogy dinamikusan irányítsd a ciklusok viselkedését.