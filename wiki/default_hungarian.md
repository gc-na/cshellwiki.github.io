# [Linux] Bash alapértelmezett parancs: Fájlok keresése

## Áttekintés
A `find` parancs lehetővé teszi fájlok és könyvtárak keresését a fájlrendszerben különböző kritériumok alapján, mint például név, típus, méret vagy módosítási idő.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
find [útvonal] [opciók] [kifejezés]
```

## Gyakori opciók
- `-name`: Keresés fájlnevek alapján.
- `-type`: Keresés fájltípus alapján (pl. `f` fájl, `d` könyvtár).
- `-size`: Keresés fájlméret alapján.
- `-mtime`: Keresés a módosítási idő alapján (pl. `-mtime -7` az elmúlt 7 napban módosított fájlokhoz).
- `-exec`: Parancs végrehajtása a megtalált fájlokon.

## Gyakori példák
1. **Fájlok keresése név alapján**:
   Keresd meg az összes `.txt` fájlt a jelenlegi könyvtárban és annak almappáiban:
   ```bash
   find . -name "*.txt"
   ```

2. **Könyvtárak keresése**:
   Keresd meg az összes könyvtárat a `/home` könyvtárban:
   ```bash
   find /home -type d
   ```

3. **Fájlok keresése méret alapján**:
   Keresd meg az összes 1 MB-nál nagyobb fájlt a `/var/log` könyvtárban:
   ```bash
   find /var/log -size +1M
   ```

4. **Módosítási idő szerinti keresés**:
   Keresd meg azokat a fájlokat, amelyeket az elmúlt 30 napban módosítottak:
   ```bash
   find . -mtime -30
   ```

5. **Parancs végrehajtása a megtalált fájlokon**:
   Töröld az összes `.tmp` fájlt a jelenlegi könyvtárban:
   ```bash
   find . -name "*.tmp" -exec rm {} \;
   ```

## Tippek
- Használj `-print` opciót, ha szeretnéd explicit módon megjeleníteni a megtalált fájlokat.
- A `-maxdepth` opcióval korlátozhatod a keresés mélységét, így elkerülheted a túl mély almappák átkutatását.
- Kombináld az opciókat a hatékonyabb keresés érdekében, például `find . -type f -size +1M -mtime -7` a nagyobb és újabb fájlok gyors kereséséhez.