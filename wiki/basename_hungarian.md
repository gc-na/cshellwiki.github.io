# [Linux] Bash basename használata: fájlnevek kinyerése

## Áttekintés
A `basename` parancs a fájlnevek kinyerésére szolgál az elérési útból. Ezzel a parancssal könnyen megkaphatjuk egy fájl vagy könyvtár nevét, anélkül, hogy az elérési út többi részét is meg kellene adnunk.

## Használat
A `basename` parancs alapvető szintaxisa a következő:

```bash
basename [opciók] [argumentumok]
```

## Gyakori Opciók
- `-a`: Több fájlnevet is megadva, mindegyikhez visszaadja a fájlnevet.
- `-s`: Megadott kiterjesztést eltávolít a fájlnévből.

## Gyakori Példák

1. **Egyszerű fájlnév kinyerése:**
   ```bash
   basename /home/felhasználó/dokumentumok/fájl.txt
   ```
   Eredmény: `fájl.txt`

2. **Kiterjesztés eltávolítása:**
   ```bash
   basename /home/felhasználó/dokumentumok/fájl.txt .txt
   ```
   Eredmény: `fájl`

3. **Több fájlnév kinyerése:**
   ```bash
   basename -a /home/felhasználó/fájl1.txt /home/felhasználó/fájl2.txt
   ```
   Eredmény:
   ```
   fájl1.txt
   fájl2.txt
   ```

4. **Kiterjesztés eltávolítása több fájlnévből:**
   ```bash
   basename -a /home/felhasználó/fájl1.txt /home/felhasználó/fájl2.txt .txt
   ```
   Eredmény:
   ```
   fájl1
   fájl2
   ```

## Tippek
- Használj `basename`-t scriptjeidben, ha csak a fájlnevekre van szükséged, így elkerülheted az elérési utak bonyolultságát.
- Ha több fájlt szeretnél egyszerre feldolgozni, a `-a` opció használata gyorsabbá teszi a munkát.
- Ne felejtsd el a kiterjesztések eltávolítását, ha csak a fájl alapnevét szeretnéd megkapni.