# [Linux] Bash bindkey használata: Billentyűparancsok kezelése

## Áttekintés
A `bindkey` parancs a Unix-alapú rendszerekben a billentyűparancsok kezelésére szolgál. Lehetővé teszi a felhasználók számára, hogy testre szabják a parancssori környezetüket, például billentyűkombinációkat rendeljenek bizonyos parancsokhoz.

## Használat
A `bindkey` parancs alapvető szintaxisa a következő:

```bash
bindkey [opciók] [argumentumok]
```

## Gyakori opciók
- `-L`: Listázza a jelenlegi billentyűparancsokat.
- `-e`: Az emacs billentyűparancsok használatára vált.
- `-v`: A vi billentyűparancsok használatára vált.
- `-s`: Szöveges parancsok hozzárendelése billentyűkombinációkhoz.

## Gyakori példák
1. **Billentyűparancsok listázása:**
   ```bash
   bindkey -L
   ```

2. **Emacs billentyűparancsok aktiválása:**
   ```bash
   bindkey -e
   ```

3. **Vi billentyűparancsok aktiválása:**
   ```bash
   bindkey -v
   ```

4. **Billentyűkombináció hozzárendelése egy parancshoz:**
   ```bash
   bindkey '^X' 'exit'
   ```

5. **Szöveges parancs hozzárendelése:**
   ```bash
   bindkey -s '^G' 'git status\n'
   ```

## Tippek
- Használj `bindkey -L` parancsot a már beállított billentyűparancsok gyors áttekintéséhez.
- Kísérletezz különböző billentyűkombinációkkal, hogy megtaláld a számodra legkényelmesebb beállítást.
- Ne felejtsd el elmenteni a beállításaidat, hogy a következő munkamenetben is elérhetők legyenek.