# [Linux] Bash break használata: A ciklusok megszakítása

## Áttekintés
A `break` parancs a Bash szkriptekben és parancssori környezetben a ciklusok (például `for`, `while`, `until`) megszakítására szolgál. Amikor a `break` parancsot végrehajtják, a vezérlés azonnal kilép a legbelsőbb ciklusból.

## Használat
A `break` parancs alapvető szintaxisa a következő:

```bash
break [n]
```

Ahol `n` a ciklusok számát jelöli, amelyeket meg szeretnénk szakítani. Alapértelmezés szerint `n` értéke 1, ami azt jelenti, hogy csak a legbelső ciklus szakad meg.

## Gyakori opciók
- `n`: Megadja, hogy hány ciklust szeretnénk megszakítani. Ha nem adunk meg értéket, akkor csak a legbelső ciklus szakad meg.

## Gyakori példák

1. **Egyszerű ciklus megszakítása:**
   ```bash
   for i in {1..5}; do
       if [ $i -eq 3 ]; then
           break
       fi
       echo $i
   done
   ```
   *Ez a példa 1-től 5-ig számol, de a 3-as számnál megszakítja a ciklust, így az eredmény 1 és 2 lesz.*

2. **While ciklus megszakítása:**
   ```bash
   count=1
   while [ $count -le 5 ]; do
       if [ $count -eq 4 ]; then
           break
       fi
       echo $count
       ((count++))
   done
   ```
   *Itt a ciklus 1-től 5-ig számol, de a 4-es számnál megszakítja a ciklust, így az eredmény 1, 2 és 3 lesz.*

3. **Több ciklus megszakítása:**
   ```bash
   for i in {1..3}; do
       for j in {1..3}; do
           if [ $i -eq 2 ]; then
               break 2
           fi
           echo "i: $i, j: $j"
       done
   done
   ```
   *Ebben a példában, amikor `i` értéke 2, mindkét ciklus megszakad, így nem lesz kimenet.*

## Tippek
- Használj `break`-et, amikor tudod, hogy egy feltétel teljesülése esetén nem szükséges a ciklus további végrehajtása.
- Ha több ciklust szeretnél megszakítani, mindig figyelj arra, hogy a `break n` szintaxis helyes legyen, ahol `n` a megszakítandó ciklusok száma.
- A `break` parancs használata segíthet a kód olvashatóságának javításában, mivel csökkenti a felesleges ciklusok számát.