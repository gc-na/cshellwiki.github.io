# [Linux] Bash diff használata: Két fájl közötti eltérések megjelenítése

## Áttekintés
A `diff` parancs a fájlok közötti eltérések összehasonlítására szolgál. Két fájl tartalmát hasonlítja össze, és megmutatja az eltéréseket, így könnyen észlelhetjük a változásokat.

## Használat
A `diff` parancs alapvető szintaxisa a következő:

```bash
diff [opciók] [fájl1] [fájl2]
```

## Gyakori opciók
- `-u`: Egységes formátumban jeleníti meg az eltéréseket, ami könnyebben olvasható.
- `-c`: Kontextus formátumban mutatja be az eltéréseket, amely több sor kontextust is tartalmaz.
- `-i`: Figyelmen kívül hagyja a kis- és nagybetűk közötti eltéréseket.
- `-w`: Figyelmen kívül hagyja a szóközök közötti eltéréseket.

## Gyakori példák
1. Két fájl egyszerű összehasonlítása:
   ```bash
   diff file1.txt file2.txt
   ```

2. Eltérések megjelenítése egységes formátumban:
   ```bash
   diff -u file1.txt file2.txt
   ```

3. Eltérések kontextus formátumban:
   ```bash
   diff -c file1.txt file2.txt
   ```

4. Kis- és nagybetűk figyelmen kívül hagyása:
   ```bash
   diff -i file1.txt file2.txt
   ```

## Tippek
- Használj `-u` opciót, ha a kimenetet szeretnéd könnyen olvasható formátumban látni, például patch fájlok létrehozásához.
- A `diff` parancs kimenetét irányíthatod fájlba, ha a `>` operátort használod, így később is visszanézheted az eltéréseket.
- Érdemes a `diff` parancsot szkriptekben használni, hogy automatizáld a fájlok összehasonlítását.