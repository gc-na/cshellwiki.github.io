# [Linux] Bash foreach használat: Ciklusok végrehajtása

## Áttekintés
A `foreach` parancs egy ciklusparancs, amely lehetővé teszi, hogy egy adott parancsot többször végrehajtsunk egy lista elemeire. Ez különösen hasznos, ha több fájlt vagy adatot szeretnénk egyszerre feldolgozni.

## Használat
A `foreach` parancs alapvető szintaxisa a következő:

```
foreach [opciók] [argumentumok]
```

## Gyakori opciók
- `-n`: Ne írja ki a parancsot a standard kimenetre, csak a kimenetet.
- `-p`: Kérdezze meg a felhasználót, mielőtt végrehajtaná a parancsot.
- `-v`: Verbose mód, amely részletesebb kimenetet ad.

## Gyakori példák
1. **Fájlok listázása és feldolgozása**:
   ```bash
   foreach file (*.txt)
       echo "Feldolgozás: $file"
   end
   ```

2. **Több parancs végrehajtása**:
   ```bash
   foreach i (1 2 3 4 5)
       echo "Szám: $i"
   end
   ```

3. **Fájlok másolása**:
   ```bash
   foreach file (*.jpg)
       cp $file /backup/
   end
   ```

## Tippek
- Mindig ellenőrizd a parancsokat, mielőtt végrehajtanád őket, különösen, ha fájlokkal dolgozol.
- Használj változókat a kód olvashatóságának javítása érdekében.
- Gyakorolj a `-n` opcióval, hogy lásd, mit fog végrehajtani a parancs, mielőtt ténylegesen futtatnád.