# [Linux] Bash find használat: Fájlok keresése

## Áttekintés
A `find` parancs lehetővé teszi fájlok és könyvtárak keresését a fájlrendszerben különböző kritériumok alapján, mint például név, típus, méret és módosítási idő.

## Használat
A `find` parancs alapvető szintaxisa a következő:

```bash
find [opciók] [érvek]
```

## Gyakori opciók
- `-name`: Keresés fájlnevek alapján.
- `-type`: Keresés fájltípus alapján (pl. `f` fájl, `d` könyvtár).
- `-size`: Keresés fájlméret alapján.
- `-mtime`: Keresés a módosítási idő alapján (napokban).
- `-exec`: Parancs végrehajtása a megtalált fájlokon.

## Gyakori példák
1. **Fájl keresése név alapján:**
   Keresd meg az összes `.txt` fájlt a jelenlegi könyvtárban és almappáiban.
   ```bash
   find . -name "*.txt"
   ```

2. **Könyvtár keresése:**
   Keresd meg az összes könyvtárat a `/home` könyvtárban.
   ```bash
   find /home -type d
   ```

3. **Fájlok keresése méret alapján:**
   Keresd meg az összes 1 MB-nál nagyobb fájlt a jelenlegi könyvtárban.
   ```bash
   find . -size +1M
   ```

4. **Fájlok keresése módosítási idő alapján:**
   Keresd meg azokat a fájlokat, amelyeket az utolsó 7 napban módosítottak.
   ```bash
   find . -mtime -7
   ```

5. **Parancs végrehajtása a megtalált fájlokon:**
   Töröld az összes `.tmp` fájlt a jelenlegi könyvtárban.
   ```bash
   find . -name "*.tmp" -exec rm {} \;
   ```

## Tippek
- Használj `-print` opciót, ha szeretnéd, hogy a `find` parancs kiírja a megtalált fájlokat.
- Kombinálj több opciót a keresési feltételek szűkítésére.
- Légy óvatos az `-exec` opció használatával, különösen törlés esetén, hogy elkerüld a nem kívánt fájlok eltávolítását.