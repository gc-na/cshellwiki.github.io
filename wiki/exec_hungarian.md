# [Linux] Bash exec használata: Folyamatok futtatása

## Áttekintés
Az `exec` parancs a Bash környezetben lehetővé teszi egy új program futtatását a jelenlegi shell folyamatában. Ez azt jelenti, hogy a shell, amelyben az `exec` parancsot futtatják, helyettesítve lesz az új programmal, így a shell nem tér vissza a parancs végrehajtása után.

## Használat
Az `exec` parancs alapvető szintaxisa a következő:

```bash
exec [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Megadhat egy alternatív nevet a programhoz.
- `-l`: A programot login shell-ként indítja el.
- `-c`: A környezeti változók törlése a program indítása előtt.

## Gyakori példák
1. **Egy program futtatása**:
   Az alábbi példa a `ls` parancsot futtatja, amely a könyvtár tartalmát listázza ki:
   ```bash
   exec ls -l
   ```

2. **Egy új shell indítása**:
   A következő példa egy új Bash shellt indít:
   ```bash
   exec bash
   ```

3. **Alternatív név megadása**:
   Az alábbi példa a `my_script.sh` fájlt futtatja, alternatív névvel:
   ```bash
   exec -a my_custom_name ./my_script.sh
   ```

4. **Környezet törlése**:
   A következő példa egy Python programot indít, törölve a környezeti változókat:
   ```bash
   exec -c python my_script.py
   ```

## Tippek
- Használja az `exec` parancsot, ha szeretné, hogy a shell folyamata helyettesítve legyen egy másik programmal, így elkerülheti a felesleges shell példányok létrehozását.
- Legyen óvatos az `exec` használatával, mert a parancs végrehajtása után nem tér vissza a shell prompt, kivéve, ha a futtatott program kifejezetten visszatér.
- Használja az `-a` opciót, ha szeretné, hogy a program más néven fusson, ami hasznos lehet a szkriptekben vagy automatizálási feladatokban.