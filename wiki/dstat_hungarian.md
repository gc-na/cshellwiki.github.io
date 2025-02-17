# [Linux] Bash dstat használata: Rendszererőforrások valós idejű megfigyelése

## Áttekintés
A `dstat` parancs egy hatékony eszköz a rendszer teljesítményének és erőforrásainak valós idejű megfigyelésére. Lehetővé teszi a felhasználók számára, hogy különböző teljesítménymutatókat, például CPU használatot, memóriahasználatot, lemez- és hálózati aktivitást figyeljenek meg egyetlen parancs segítségével.

## Használat
A `dstat` parancs alapvető szintaxisa a következő:

```bash
dstat [opciók] [argumentumok]
```

## Gyakori Opciók
- `-c`: CPU statisztikák megjelenítése.
- `-d`: Lemez statisztikák megjelenítése.
- `-n`: Hálózati statisztikák megjelenítése.
- `-m`: Memória statisztikák megjelenítése.
- `-t`: Időbélyeg megjelenítése a kimenetben.

## Gyakori Példák
1. **Alapvető rendszerfigyelés**:
   ```bash
   dstat
   ```

2. **CPU és memória használat figyelése**:
   ```bash
   dstat -c -m
   ```

3. **Lemez és hálózati aktivitás megjelenítése**:
   ```bash
   dstat -d -n
   ```

4. **Időbélyeggel ellátott teljesítménystatisztikák**:
   ```bash
   dstat -t
   ```

5. **Összes erőforrás figyelése**:
   ```bash
   dstat -cdmn
   ```

## Tippek
- Használj több opciót egyszerre a részletesebb megfigyelés érdekében.
- A `dstat` kimenetét irányíthatod fájlba a `>` operátor segítségével, így később elemezheted az adatokat.
- A `--help` opcióval megtekintheted a parancs összes elérhető opcióját és azok leírását.