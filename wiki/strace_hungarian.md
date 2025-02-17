# [Linux] Bash strace használata: Rendszerhívások nyomozása

## Áttekintés
A `strace` parancs egy hasznos eszköz, amely lehetővé teszi a felhasználók számára, hogy nyomon követhessék a programok által végrehajtott rendszerhívásokat és jeleket. Ez segít a hibakeresésben és a programok működésének megértésében.

## Használat
A `strace` parancs alapvető szintaxisa a következő:

```bash
strace [opciók] [argumentumok]
```

## Gyakori opciók
- `-e`: Különböző rendszerhívások szűrése.
- `-o`: Kimeneti fájl megadása, ahová a nyomozási információkat menti.
- `-p`: Egy már futó folyamat nyomozása a folyamat azonosítója (PID) alapján.
- `-c`: Összegző statisztikák megjelenítése a hívásokról.

## Gyakori példák
1. **Alapvető nyomozás egy programról:**
   ```bash
   strace ls
   ```

2. **Kimenet mentése fájlba:**
   ```bash
   strace -o output.txt ls
   ```

3. **Folyamat nyomozása PID alapján:**
   ```bash
   strace -p 1234
   ```

4. **Csak a fájlokkal kapcsolatos hívások nyomozása:**
   ```bash
   strace -e trace=file ls
   ```

5. **Összegző statisztikák megjelenítése:**
   ```bash
   strace -c ls
   ```

## Tippek
- Használj `-o` opciót, hogy a kimenetet fájlba mentsd, így könnyebben elemezheted később.
- A `-e` opcióval szűkítheted a nyomozást, hogy csak a releváns hívásokat lásd.
- A `strace` futtatása rendszergazdai jogosultságokat igényelhet bizonyos folyamatok esetén, ezért érdemes sudo-t használni, ha szükséges.