# [Linux] Bash grep használata: Szöveg keresése fájlokban

## Áttekintés
A `grep` parancs egy rendkívül hasznos eszköz a szöveges fájlokban történő kereséshez. Lehetővé teszi a felhasználók számára, hogy mintákat keressenek a fájlokban, és csak azokat a sorokat jelenítse meg, amelyek megfelelnek a keresett kifejezésnek.

## Használat
A `grep` parancs alapvető szintaxisa a következő:

```bash
grep [opciók] [kifejezés] [fájlok]
```

## Gyakori opciók
- `-i`: Nagy- és kisbetű érzéketlen keresés.
- `-v`: Azokat a sorokat mutatja, amelyek nem tartalmazzák a megadott kifejezést.
- `-r`: Rekurzív keresés a megadott könyvtárban.
- `-n`: A találatok sorainak számát is megjeleníti.
- `-l`: Csak a fájlneveket listázza, amelyek tartalmazzák a keresett kifejezést.

## Gyakori példák
1. **Egyszerű keresés egy fájlban:**

```bash
grep "keresett_kifejezés" fajl.txt
```

2. **Keresés több fájlban:**

```bash
grep "keresett_kifejezés" *.txt
```

3. **Nagy- és kisbetű érzéketlen keresés:**

```bash
grep -i "keresett_kifejezés" fajl.txt
```

4. **Sorok számának megjelenítése:**

```bash
grep -n "keresett_kifejezés" fajl.txt
```

5. **Rekurzív keresés egy könyvtárban:**

```bash
grep -r "keresett_kifejezés" /elérési/út/
```

## Tippek
- Használj reguláris kifejezéseket a keresési minták pontosabbá tételéhez.
- Kombináld a `grep` parancsot más parancsokkal, például a `pipe` (`|`) segítségével, hogy hatékonyabb kereséseket végezhess.
- Ellenőrizd a fájlok tartalmát a `cat` vagy `less` parancsokkal, mielőtt a `grep`-et használnád, hogy tudd, mit keresel.