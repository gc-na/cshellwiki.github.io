# [Linux] Bash modprobe használata: Modulok betöltése és eltávolítása

## Áttekintés
A `modprobe` parancs a Linux operációs rendszerekben használt eszköz, amely lehetővé teszi a kernel modulok betöltését és eltávolítását. Ez a parancs automatikusan kezeli a modulok függőségeit, így egyszerűsíti a modulok kezelését.

## Használat
A `modprobe` parancs alapvető szintaxisa a következő:

```bash
modprobe [opciók] [argumentumok]
```

## Gyakori opciók
- `-r`, `--remove`: Eltávolítja a megadott modult.
- `-n`, `--dry-run`: Szimulálja a parancs végrehajtását anélkül, hogy ténylegesen végrehajtaná.
- `-v`, `--verbose`: Részletes kimenetet ad a parancs végrehajtásáról.

## Gyakori példák
1. **Modul betöltése**:
   A `dummy` modul betöltéséhez használja a következő parancsot:
   ```bash
   modprobe dummy
   ```

2. **Modul eltávolítása**:
   A `dummy` modul eltávolításához a következő parancsot kell kiadni:
   ```bash
   modprobe -r dummy
   ```

3. **Szimulált végrehajtás**:
   A `dummy` modul betöltésének szimulálásához:
   ```bash
   modprobe -n dummy
   ```

4. **Részletes kimenet**:
   A `dummy` modul betöltése részletes kimenettel:
   ```bash
   modprobe -v dummy
   ```

## Tippek
- Mindig ellenőrizze a modulok függőségeit, mielőtt eltávolítaná őket, hogy elkerülje a rendszer instabilitását.
- Használja a `--dry-run` opciót, ha nem biztos abban, hogy a parancs mit fog tenni.
- Rendszeresen frissítse a kernel modulok listáját, hogy a legújabb verziókat használja.