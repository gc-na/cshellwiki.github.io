# [Linux] Bash chmod használata: Fájlok és könyvtárak jogosultságainak módosítása

## Áttekintés
A `chmod` parancs a fájlok és könyvtárak jogosultságainak módosítására szolgál a Unix-alapú operációs rendszerekben. Ezzel a paranccsal beállíthatjuk, hogy ki olvashatja, írhatja vagy futtathatja a fájlokat.

## Használat
A `chmod` parancs alapvető szintaxisa a következő:

```bash
chmod [opciók] [argumentumok]
```

## Gyakori opciók
- `u`: a fájl tulajdonosa (user)
- `g`: a fájl csoportja (group)
- `o`: más felhasználók (others)
- `a`: mindenki (all)
- `+`: jogosultság hozzáadása
- `-`: jogosultság eltávolítása
- `=`: jogosultság beállítása

## Gyakori példák
1. **Olvasási jogosultság hozzáadása a tulajdonoshoz:**
   ```bash
   chmod u+r fájl.txt
   ```

2. **Írási jogosultság eltávolítása a csoporttól:**
   ```bash
   chmod g-w fájl.txt
   ```

3. **Futtatási jogosultság beállítása minden felhasználónak:**
   ```bash
   chmod a+x fájl.sh
   ```

4. **Összes jogosultság eltávolítása más felhasználóktól:**
   ```bash
   chmod o-rwx fájl.txt
   ```

5. **Jogosultságok beállítása numerikus módszerrel (pl. 755):**
   ```bash
   chmod 755 fájl.txt
   ```

## Tippek
- Mindig ellenőrizd a fájl jogosultságait a `ls -l` paranccsal, mielőtt módosítanád őket.
- Használj numerikus módszert, ha gyorsan szeretnéd beállítani a jogosultságokat.
- Légy óvatos a `chmod` használatával, különösen a `777` jogosultság beállításakor, mivel ez mindenki számára teljes hozzáférést ad.