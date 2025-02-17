# [Linux] Bash batch használata: Feladatok ütemezése

## Áttekintés
A `batch` parancs lehetővé teszi, hogy a felhasználók ütemezett feladatokat hajtsanak végre a rendszer terheltségétől függően. Az ütemezett feladatok a rendszer terheltsége csökkenésekor kerülnek végrehajtásra, így ideális megoldás lehet hosszabb ideig tartó vagy erőforrás-igényes műveletekhez.

## Használat
A `batch` parancs alapvető szintaxisa a következő:

```bash
batch [opciók] [argumentumok]
```

## Gyakori opciók
- `-l`, `--login`: A parancsot bejelentkezési környezetben futtatja.
- `-p`, `--print`: Kiírja a parancsot a standard kimenetre, de nem hajtja végre.
- `-h`, `--help`: Megjeleníti a súgót és a parancs használatát.

## Gyakori példák
1. **Egyszerű feladat ütemezése**:
   A következő parancs egy egyszerű shell parancsot ütemez a rendszer terheltsége csökkenésekor:
   ```bash
   echo "echo 'Hello, World!'" | batch
   ```

2. **Fájl tartalmának kiírása**:
   A következő példa egy fájl tartalmát írja ki a terminálra, amikor a rendszer terheltsége engedi:
   ```bash
   cat /path/to/file.txt | batch
   ```

3. **Több parancs ütemezése**:
   Több parancsot is ütemezhetünk egyszerre:
   ```bash
   echo "command1; command2; command3" | batch
   ```

## Tippek
- Használja a `-l` opciót, ha a parancsoknak bejelentkezési környezetre van szükségük.
- Ellenőrizze a `atq` parancsot a várakozó feladatok listázásához.
- Használja a `atrm` parancsot a már ütemezett feladatok eltávolításához, ha már nincs szüksége rájuk.