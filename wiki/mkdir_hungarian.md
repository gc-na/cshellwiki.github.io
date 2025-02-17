# [Linux] Bash mkdir használata: Mappák létrehozása

## Áttekintés
A `mkdir` parancs a Bash környezetben új mappák (könyvtárak) létrehozására szolgál. Ez a parancs lehetővé teszi a felhasználók számára, hogy rendszerezzék fájljaikat és mappáikat.

## Használat
A `mkdir` parancs alapvető szintaxisa a következő:

```bash
mkdir [opciók] [argumentumok]
```

## Gyakori opciók
- `-p`: Létrehozza a szülő mappákat is, ha azok még nem léteznek.
- `-v`: Részletes kimenetet ad, amely megmutatja, hogy mely mappák lettek létrehozva.
- `-m`: Beállítja a mappa jogosultságait a létrehozáskor.

## Gyakori példák
1. **Egyszerű mappa létrehozása:**
   ```bash
   mkdir uj_mappa
   ```

2. **Több mappa létrehozása egyszerre:**
   ```bash
   mkdir mappa1 mappa2 mappa3
   ```

3. **Szülő mappák létrehozása a `-p` opcióval:**
   ```bash
   mkdir -p szulo_mappa/gyerek_mappa
   ```

4. **Részletes kimenet megjelenítése a `-v` opcióval:**
   ```bash
   mkdir -v uj_mappa
   ```

5. **Mappa jogosultságainak beállítása a `-m` opcióval:**
   ```bash
   mkdir -m 755 uj_mappa
   ```

## Tippek
- Mindig ellenőrizd, hogy a mappa, amelyet létre szeretnél hozni, még nem létezik, hogy elkerüld a hibákat.
- Használj `-p` opciót, ha nem vagy biztos benne, hogy a szülő mappák léteznek.
- A mappák létrehozása előtt érdemes megnyitni a terminált a kívánt könyvtárban, ahol a mappát létre szeretnéd hozni.