# [Linux] Bash printf használata: Szövegek formázása és kiírása

## Áttekintés
A `printf` parancs a Bash környezetben a szövegek formázott kiírására szolgál. Lehetővé teszi a felhasználók számára, hogy pontosan meghatározzák, hogyan jelenjenek meg a szövegek, számok és egyéb adatok a terminálon.

## Használat
A `printf` parancs alapvető szintaxisa a következő:

```bash
printf [opciók] [formátum] [argumentumok]
```

## Gyakori opciók
- `-v`: Változóba menti a kimenetet.
- `--help`: Megjeleníti a parancs használati útmutatóját.
- `--version`: Megjeleníti a `printf` verzióját.

## Gyakori példák

1. **Egyszerű szöveg kiírása:**
   ```bash
   printf "Helló, világ!\n"
   ```

2. **Számok formázása:**
   ```bash
   printf "A szám: %d\n" 42
   ```

3. **Több argumentum kiírása:**
   ```bash
   printf "Név: %s, Kor: %d\n" "Anna" 30
   ```

4. **Tizedesjegyek megjelenítése:**
   ```bash
   printf "Pi értéke: %.2f\n" 3.14159
   ```

5. **Tömb elemeinek kiírása:**
   ```bash
   array=(1 2 3 4 5)
   printf "Tömb elemei: %d\n" "${array[@]}"
   ```

## Tippek
- Használj formátum specifikátorokat a megjelenítés testreszabásához, mint például `%s` (szöveg), `%d` (egész szám) és `%.2f` (tizedes szám).
- Ne felejtsd el a `\n` karaktert a sorok végén, hogy új sort kezdj a kimenetben.
- A `printf` parancs használata előnyösebb lehet, mint az `echo`, mivel pontosabb formázást tesz lehetővé.