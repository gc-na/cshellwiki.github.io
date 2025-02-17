# [Linux] Bash tr használata: Karakterek átkonvertálása

## Áttekintés
A `tr` parancs a Unix-alapú rendszerekben karakterek átkonvertálására szolgál. Lehetővé teszi a karakterek cseréjét, törlését vagy másolását a bemeneti adatfolyamban.

## Használat
A `tr` parancs alapvető szintaxisa a következő:

```bash
tr [opciók] [argumentumok]
```

## Gyakori opciók
- `-d`: Törli a megadott karaktereket a bemeneti adatfolyamból.
- `-s`: Összenyomja a megadott karakterek ismétlődéseit egyetlen karakterré.
- `-c`: A megadott karakterek kiegészítő halmazát használja.

## Gyakori példák
1. **Karakterek cseréje**: Az összes kisbetűt nagybetűvé alakít.
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```

2. **Karakterek törlése**: Az összes számjegy eltávolítása a szövegből.
   ```bash
   echo "abc123def456" | tr -d '0-9'
   ```

3. **Ismétlődő szóközök eltávolítása**: Az ismétlődő szóközöket egyetlen szóközre cseréli.
   ```bash
   echo "This    is    a    test." | tr -s ' '
   ```

4. **Karakterek kiegészítése**: A kisbetűs karakterek nagybetűs megfelelőjére cserélése, miközben a nem kisbetűs karakterek változatlanok maradnak.
   ```bash
   echo "Hello World 123!" | tr 'a-z' 'A-Z'
   ```

## Tippek
- Használj csővezetékeket (`|`) a `tr` parancs kombinálására más parancsokkal, hogy hatékonyabb adatfeldolgozást végezz.
- Ellenőrizd a bemeneti adatokat, mielőtt alkalmaznád a `-d` opciót, hogy elkerüld a fontos karakterek véletlen törlését.
- Használj `echo` parancsot a teszteléshez, hogy gyorsan kipróbálhasd a `tr` parancsot anélkül, hogy fájlokat kellene létrehoznod.