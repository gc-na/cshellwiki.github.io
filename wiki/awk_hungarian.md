# [Linux] Bash awk használata: Szövegfeldolgozás és mintakeresés

## Áttekintés
Az `awk` egy erőteljes szövegfeldolgozó eszköz, amely lehetővé teszi a fájlok és szövegek sorainak és mezőinek feldolgozását. Az `awk` programozási nyelvként is működik, amely lehetővé teszi a bonyolultabb adatfeldolgozási feladatok elvégzését.

## Használat
Az `awk` parancs alapvető szintaxisa a következő:

```bash
awk [opciók] [argumentumok]
```

## Gyakori opciók
- `-F`: Megadja a mezőelválasztót (pl. `-F,` a CSV fájlokhoz).
- `-v`: Változók definiálására szolgál a parancs futtatása előtt.
- `-f`: Külső fájlban található `awk` program futtatása.
- `-e`: Az `awk` program közvetlen megadása parancssorban.

## Gyakori példák

1. **Egyszerű mezőkiírás**
   Kiírja a második mezőt egy fájl minden sorából:
   ```bash
   awk '{print $2}' fajl.txt
   ```

2. **Mezőelválasztó megadása**
   CSV fájl második mezőjének kiírása:
   ```bash
   awk -F, '{print $2}' fajl.csv
   ```

3. **Változó használata**
   Sorok számának megszámlálása:
   ```bash
   awk -v count=0 '{count++} END {print count}' fajl.txt
   ```

4. **Feltételes kiírás**
   Csak azokat a sorokat írja ki, ahol az első mező "John":
   ```bash
   awk '$1 == "John" {print}' fajl.txt
   ```

5. **Összegzés**
   Az első mező számértékeinek összege:
   ```bash
   awk '{sum += $1} END {print sum}' fajl.txt
   ```

## Tippek
- Használj mezőelválasztót, ha a bemeneti fájl nem szóközökkel van elválasztva.
- A `BEGIN` és `END` blokkok használatával előkészítheted a környezetet és összegzéseket végezhetsz.
- Próbáld ki az `awk` parancsot pipelininggal más parancsokkal, mint például `grep` vagy `sort`, hogy még hatékonyabb adatfeldolgozást végezhess.