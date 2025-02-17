# [Linux] Bash lsblk használata: A blokkeszközök listázása

## Áttekintés
Az `lsblk` parancs a Linux operációs rendszerben a blokkeszközök, például merevlemezek, SSD-k és partíciók listázására szolgál. Ez a parancs segít megérteni a rendszer tárolóeszközeinek felépítését és állapotát.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
lsblk [opciók] [argumentumok]
```

## Gyakori opciók
- `-a` vagy `--all`: Minden blokkeszközt megjelenít, beleértve azokat is, amelyek nem csatoltak.
- `-f` vagy `--fs`: Megjeleníti a fájlrendszer típusát és a címkéket.
- `-l` vagy `--list`: Lista formátumban jeleníti meg az eszközöket.
- `-o` vagy `--output`: Lehetővé teszi a megjelenítendő oszlopok testreszabását.
- `-p` vagy `--paths`: Az eszközök teljes elérési útját mutatja.

## Gyakori példák
1. **Alapvető blokkeszközök listázása:**
   ```bash
   lsblk
   ```

2. **Minden blokkeszköz megjelenítése, beleértve a nem csatoltakat is:**
   ```bash
   lsblk -a
   ```

3. **Fájlrendszer típusának és címkéjének megjelenítése:**
   ```bash
   lsblk -f
   ```

4. **Lista formátumban történő megjelenítés:**
   ```bash
   lsblk -l
   ```

5. **Csak a megadott oszlopok megjelenítése:**
   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

## Tippek
- Használja az `-f` opciót, ha szeretné gyorsan ellenőrizni a fájlrendszer típusát és a partíciók címkéit.
- A `-o` opcióval testreszabhatja a megjelenítést, hogy csak a legfontosabb információkat lássa.
- A `lsblk` parancs kimenete jól használható más parancsokkal, például a `grep`-pel, ha specifikus információkat keres.