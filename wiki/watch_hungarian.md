# [Linux] Bash watch használata: Az parancs folyamatos végrehajtása

## Áttekintés
A `watch` parancs lehetővé teszi, hogy egy adott parancsot folyamatosan végrehajtsunk, és az eredményét időszakosan frissítsük a terminálban. Ez hasznos lehet, ha szeretnénk nyomon követni a rendszer állapotát vagy egy adott parancs kimenetét.

## Használat
A `watch` parancs alapvető szintaxisa a következő:

```bash
watch [opciók] [parancs]
```

## Gyakori opciók
- `-n, --interval`: Megadja a frissítési időközt másodpercben. Alapértelmezett érték 2 másodperc.
- `-d, --differences`: Kiemeli a változásokat a parancs kimenetében.
- `-t, --no-title`: Elrejti a fejlécet, így csak a parancs kimenete látható.

## Gyakori példák
1. A rendszer állapotának nyomon követése:
   ```bash
   watch -n 5 free -h
   ```
   Ez a parancs 5 másodpercenként frissíti a memóriahasználatot.

2. Folyamatok figyelése:
   ```bash
   watch -n 2 ps aux
   ```
   Ezzel a parancssal 2 másodpercenként láthatjuk a futó folyamatokat.

3. Fájlok méretének nyomon követése:
   ```bash
   watch -d du -sh /path/to/directory
   ```
   Ez kiemeli a változásokat a megadott könyvtár méretében.

4. Hálózati kapcsolat ellenőrzése:
   ```bash
   watch -n 1 ifconfig
   ```
   Ez 1 másodpercenként frissíti a hálózati interfészek állapotát.

## Tippek
- Használj rövidebb frissítési időt, ha gyors változásokat szeretnél nyomon követni, de figyelj arra, hogy ez nagyobb terhelést jelenthet a rendszerre.
- A `-d` opció használata segíthet gyorsan észlelni a változásokat, különösen, ha sok adatot nézel.
- Ha csak a parancs kimenetére vagy kíváncsi, a `-t` opcióval elrejtheted a fejlécet, így tisztább nézetet kapsz.