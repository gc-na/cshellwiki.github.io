# [Linux] Bash @ használata: Fájlok keresése

## Áttekintés
A `find` parancs lehetővé teszi fájlok és könyvtárak keresését a fájlrendszerben különböző kritériumok alapján. Használható fájlnevek, típusok, méretek és egyéb attribútumok szerint történő keresésre.

## Használat
A `find` parancs alapvető szintaxisa a következő:

```bash
find [útvonal] [opciók] [kifejezés]
```

## Gyakori opciók
- `-name`: Keresés fájlnevek alapján.
- `-type`: Keresés fájltípus alapján (pl. `f` fájl, `d` könyvtár).
- `-size`: Keresés fájlméret alapján (pl. `+100k` 100 KB-nál nagyobb fájlok).
- `-mtime`: Keresés fájlok módosítási ideje alapján (pl. `-1` az utolsó 24 órában módosított fájlokhoz).
- `-exec`: Parancs végrehajtása a megtalált fájlokon.

## Gyakori példák
1. Fájlok keresése név alapján:

```bash
find /home/user -name "dokumentum.txt"
```

2. Minden könyvtár keresése a `/var` könyvtárban:

```bash
find /var -type d
```

3. 100 KB-nál nagyobb fájlok keresése:

```bash
find / -size +100k
```

4. Az utolsó 7 napban módosított fájlok keresése:

```bash
find /home/user -mtime -7
```

5. Fájlok törlése a megtalált fájlok alapján:

```bash
find /tmp -name "*.tmp" -exec rm {} \;
```

## Tippek
- Használj relatív vagy abszolút útvonalakat a pontos keresés érdekében.
- A `-print` opciót nem szükséges megadni, mivel az alapértelmezett viselkedés.
- A `-exec` opció használatakor mindig zárd le a parancsot `\;` karakterekkel.
- A `-maxdepth` opcióval korlátozhatod a keresés mélységét, így gyorsabbá teheted a keresést nagy fájlrendszerekben.