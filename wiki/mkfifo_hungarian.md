# [Linux] Bash mkfifo használat: Fájlok létrehozása FIFO (First In First Out) típusú csatornákhoz

## Áttekintés
A `mkfifo` parancs lehetővé teszi, hogy FIFO (First In First Out) típusú csatornákat hozzunk létre a Linux rendszeren. Ezek a csatornák lehetővé teszik, hogy az adatok egy folyamatból egy másikba áramoljanak, anélkül hogy fájlokat kellene létrehozni.

## Használat
A `mkfifo` parancs alapvető szintaxisa a következő:

```bash
mkfifo [opciók] [argumentumok]
```

## Gyakori opciók
- `-m, --mode=MODE`: Beállítja a FIFO fájl jogosultságait a megadott MODE szerint.
- `--help`: Megjeleníti a parancs használati útmutatóját.
- `--version`: Megjeleníti a parancs verzióját.

## Gyakori példák
1. FIFO csatorna létrehozása alapértelmezett névvel:
    ```bash
    mkfifo myfifo
    ```

2. FIFO csatorna létrehozása specifikus jogosultságokkal:
    ```bash
    mkfifo -m 600 myfifo
    ```

3. Több FIFO csatorna létrehozása egyszerre:
    ```bash
    mkfifo fifo1 fifo2 fifo3
    ```

4. FIFO csatorna létrehozása és azonnali írás:
    ```bash
    echo "Hello, World!" > myfifo &
    ```

5. FIFO csatorna olvasása egy másik terminálban:
    ```bash
    cat myfifo
    ```

## Tippek
- Mindig ellenőrizd a FIFO csatorna jogosultságait, hogy biztosítsd a megfelelő hozzáférést.
- Használj háttérfolyamatokat (`&`), hogy a FIFO csatornákkal való munka során ne blokkolódjon a terminál.
- Ne felejtsd el, hogy a FIFO csatornák nem tárolják az adatokat, így ha nincs aktív olvasó, az írási műveletek blokkolódni fognak.