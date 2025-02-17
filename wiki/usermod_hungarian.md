# [Linux] Bash usermod használata: Felhasználói fiók módosítása

## Áttekintés
A `usermod` parancs a Linux rendszerekben a felhasználói fiókok módosítására szolgál. Ezzel a paranccsal különböző beállításokat, például a felhasználói csoportokat, a jelszót, a felhasználónévhez tartozó információkat és más attribútumokat lehet megváltoztatni.

## Használat
A `usermod` parancs alapvető szintaxisa a következő:

```bash
usermod [opciók] [felhasználónév]
```

## Gyakori opciók
- `-aG`: Hozzáadja a felhasználót a megadott csoporthoz anélkül, hogy eltávolítaná a meglévő csoportokból.
- `-d`: Megváltoztatja a felhasználó otthoni könyvtárát.
- `-l`: Megváltoztatja a felhasználó nevét.
- `-s`: Megváltoztatja a felhasználó alapértelmezett shell-jét.
- `-u`: Megváltoztatja a felhasználó azonosítóját (UID).

## Gyakori példák
1. **Felhasználó hozzáadása egy csoporthoz**:
   ```bash
   usermod -aG sudo felhasználónév
   ```

2. **Felhasználói név megváltoztatása**:
   ```bash
   usermod -l újfelhasználónév régiFelhasználónév
   ```

3. **Otthoni könyvtár módosítása**:
   ```bash
   usermod -d /új/otthoni/könyvtár felhasználónév
   ```

4. **Alapértelmezett shell megváltoztatása**:
   ```bash
   usermod -s /bin/zsh felhasználónév
   ```

5. **Felhasználó UID-jának megváltoztatása**:
   ```bash
   usermod -u 1001 felhasználónév
   ```

## Tippek
- Mindig készíts biztonsági másolatot a felhasználói fiókokról, mielőtt módosításokat végeznél.
- Használj `sudo`-t a `usermod` parancs végrehajtásához, mivel rendszergazdai jogosultságokra van szükség.
- Ellenőrizd a módosításokat a `id felhasználónév` paranccsal, hogy megbizonyosodj arról, hogy a változtatások sikeresek voltak.