# [Linux] Bash socat használata: Adatfolyamok átkonvertálása és irányítása

## Áttekintés
A `socat` (SOcket CAT) egy rendkívül sokoldalú parancs, amely lehetővé teszi különböző adatfolyamok közötti kapcsolat létrehozását és azok átkonvertálását. Használható TCP/IP, UNIX domain socketek, fájlok, és sok más típusú adatfolyam kezelésére.

## Használat
A `socat` parancs alapvető szintaxisa a következő:

```bash
socat [opciók] [argumentumok]
```

## Gyakori opciók
- `-u`: Csak olvasás, nem ír.
- `-v`: Verbose (részletes) mód, amely több információt ad a folyamatokról.
- `TCP:<cím>:<port>`: TCP kapcsolat létrehozása a megadott címre és portra.
- `FILE:<fájl>`: Fájl használata bemenetként vagy kimenetként.

## Gyakori példák
1. **TCP kapcsolat létrehozása**:
   ```bash
   socat - TCP:example.com:80
   ```
   Ez a parancs TCP kapcsolatot létesít az `example.com` weboldal 80-as portjával.

2. **Adatok átkonvertálása fájl és TCP között**:
   ```bash
   socat FILE:input.txt TCP:example.com:80
   ```
   Ezzel a paranccsal az `input.txt` fájl tartalmát elküldjük az `example.com` 80-as portjára.

3. **UNIX domain socket használata**:
   ```bash
   socat UNIX-LISTEN:/tmp/mysocket.sock,fork EXEC:/path/to/script.sh
   ```
   Ez a parancs létrehoz egy UNIX socketet, amely a `script.sh` fájlt futtatja, amikor egy kapcsolat érkezik.

## Tippek
- Mindig ellenőrizd a `socat` verzióját és a dokumentációt, hogy megismerd az elérhető opciókat.
- Használj `-v` opciót a hibakereséshez, hogy részletesebb információkat kapj a kapcsolatról.
- Ha gyakran használsz `socat`-ot, érdemes lehet alias-t létrehozni a parancsok egyszerűsítésére.