# [Linux] Bash sort használata: Adatok rendezése

## Áttekintés
A `sort` parancs a fájlokban vagy a standard bemeneten található sorok rendezésére szolgál. A rendezés alapértelmezés szerint ábécé sorrendben történik, de számos lehetőség áll rendelkezésre a rendezési kritériumok testreszabására.

## Használat
A `sort` parancs alapvető szintaxisa a következő:

```bash
sort [opciók] [argumentumok]
```

## Gyakori opciók
- `-r`: Fordított sorrendben rendez.
- `-n`: Számok szerint rendez.
- `-k`: Megadott kulcs szerint rendez.
- `-u`: Csak az egyedi sorokat tartalmazza.
- `-o`: A rendezett kimenetet egy fájlba írja.

## Gyakori példák
1. **Alapértelmű rendezés**:
   ```bash
   sort fájl.txt
   ```

2. **Fordított sorrendben történő rendezés**:
   ```bash
   sort -r fájl.txt
   ```

3. **Számok szerinti rendezés**:
   ```bash
   sort -n számok.txt
   ```

4. **Több kulcs szerinti rendezés**:
   ```bash
   sort -k 2,2 -k 1,1 fájl.txt
   ```

5. **Egyedi sorok kiírása**:
   ```bash
   sort -u fájl.txt
   ```

6. **Kimenet fájlba írása**:
   ```bash
   sort -o rendezett.txt fájl.txt
   ```

## Tippek
- Használj `-n` opciót, ha számokat tartalmazó sorokat szeretnél helyesen rendezni.
- A `-k` opcióval pontosan megadhatod, hogy melyik oszlop szerint szeretnél rendezni.
- Ha nagy fájlokkal dolgozol, érdemes a `-S` opciót használni a memóriahasználat optimalizálására.