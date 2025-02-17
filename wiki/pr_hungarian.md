# [Linux] Bash pr használata: Szövegformázás és oldalszámozás

## Áttekintés
A `pr` parancs a szöveges fájlok formázására szolgál, lehetővé téve azok oldalszámozását és oszlopokba rendezését. Ezzel a paranccsal a szöveges fájlok könnyebben olvashatóvá válnak, különösen nyomtatás előtt.

## Használat
A `pr` parancs alapvető szintaxisa a következő:

```bash
pr [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Fejléc megadása, amely a kimenet tetején jelenik meg.
- `-l`: Megadja, hogy hány sort szeretnénk megjeleníteni egy oldalon.
- `-t`: A fejléc és a lábléc eltávolítása a kimenetből.
- `-s`: A szavak közötti elválasztó karakter megadása.

## Gyakori példák
1. **Alapértelmezett használat**: A `file.txt` fájl formázása.
   ```bash
   pr file.txt
   ```

2. **Fejléc megadása**: A kimenet tetején megjelenő fejléc hozzáadása.
   ```bash
   pr -h "Fejléc szöveg" file.txt
   ```

3. **Oldalszám megadása**: 30 sor megjelenítése egy oldalon.
   ```bash
   pr -l 30 file.txt
   ```

4. **Több fájl formázása**: Két fájl egyesítése és formázása.
   ```bash
   pr file1.txt file2.txt
   ```

5. **Szavak közötti elválasztó karakter megadása**: Tabulátor használata.
   ```bash
   pr -s "\t" file.txt
   ```

## Tippek
- Használj `-t` opciót, ha csak a szöveget szeretnéd látni, fejléc és lábléc nélkül.
- Kísérletezz a `-l` opcióval, hogy megtaláld a legmegfelelőbb oldalméretet a dokumentumodhoz.
- Ha több fájlt formázol, ügyelj arra, hogy a fájlok sorrendje befolyásolja a kimenetet.