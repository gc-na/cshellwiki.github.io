# [Linux] Bash script használata: Parancsok rögzítése

## Áttekintés
A `script` parancs lehetővé teszi a felhasználók számára, hogy rögzítsenek egy terminál sessiont, amelyet később vissza lehet nézni. Ez hasznos lehet, ha dokumentálni szeretnénk a parancsok futtatását vagy a terminálban végzett tevékenységeket.

## Használat
A `script` parancs alapvető szintaxisa a következő:

```bash
script [opciók] [fájl]
```

## Gyakori opciók
- `-a`: Az alapértelmezett fájlhoz hozzáfűzi a kimenetet, ahelyett, hogy felülírná.
- `-c`: Egy adott parancsot futtat, és annak kimenetét rögzíti.
- `-f`: Azonnal kiírja a kimenetet a fájlba, így valós időben követhetjük a folyamatot.
- `-q`: Csendes üzemmód, amely nem ír ki információt a terminálra a rögzítés megkezdésekor.

## Gyakori példák

1. **Alapértelmű session rögzítése**:
   ```bash
   script
   ```
   Ez elindít egy új sessiont, és a kimenetet a `typescript` nevű fájlba menti.

2. **Session rögzítése egy adott fájlba**:
   ```bash
   script mysession.txt
   ```
   A session kimenete a `mysession.txt` fájlba kerül.

3. **Egy parancs rögzítése**:
   ```bash
   script -c "ls -l" output.txt
   ```
   Ez a parancs végrehajtja az `ls -l` parancsot, és a kimenetet az `output.txt` fájlba menti.

4. **Valós idejű kimenet rögzítése**:
   ```bash
   script -f mysession.log
   ```
   Ez a parancs valós időben rögzíti a sessiont a `mysession.log` fájlba.

## Tippek
- Mindig ellenőrizd a rögzített fájl tartalmát, hogy megbizonyosodj arról, hogy minden szükséges információt rögzítettél.
- Használj egyedi fájlneveket, hogy könnyen azonosíthasd a különböző sessionöket.
- Ha hosszú parancsokat futtatsz, érdemes a `-f` opciót használni, hogy azonnal láthasd a kimenetet.