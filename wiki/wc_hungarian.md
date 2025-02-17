# [Linux] Bash wc használat: Szövegfájlok sor-, szó- és karakterszámlálása

## Áttekintés
A `wc` (word count) parancs a Unix-alapú rendszerekben használt eszköz, amely lehetővé teszi a fájlokban található sorok, szavak és karakterek számának gyors és egyszerű megszámlálását.

## Használat
A `wc` parancs alapvető szintaxisa a következő:

```bash
wc [opciók] [fájlok]
```

## Gyakori opciók
- `-l`: Csak a sorok számát adja vissza.
- `-w`: Csak a szavak számát adja vissza.
- `-c`: Csak a karakterek számát adja vissza.
- `-m`: A karakterek számát adja vissza, figyelembe véve a multibyte karaktereket is.
- `-L`: A leghosszabb sor hosszát adja vissza.

## Gyakori példák
1. **Sorok számának megjelenítése egy fájlban:**
   ```bash
   wc -l fájl.txt
   ```

2. **Szavak számának megjelenítése egy fájlban:**
   ```bash
   wc -w fájl.txt
   ```

3. **Karakterek számának megjelenítése egy fájlban:**
   ```bash
   wc -c fájl.txt
   ```

4. **Több fájl sor-, szó- és karakterszámának megjelenítése:**
   ```bash
   wc fájl1.txt fájl2.txt
   ```

5. **A leghosszabb sor hosszának megjelenítése egy fájlban:**
   ```bash
   wc -L fájl.txt
   ```

## Tippek
- Használj több opciót együtt, például `wc -l -w fájl.txt`, ha egyszerre szeretnéd látni a sorok és szavak számát.
- Ha a kimenetet egy másik parancsnak szeretnéd átadni, használj csöveket (`|`), például: `cat fájl.txt | wc -l`.
- A `wc` parancs kimenete könnyen használható szkriptekben is, hogy automatikusan feldolgozd a fájlok statisztikáit.