# [Linux] Bash env használata: környezeti változók kezelése

## Áttekintés
Az `env` parancs lehetővé teszi a környezeti változók megjelenítését és módosítását, valamint új programok futtatását a megadott környezeti beállításokkal. Hasznos eszköz a környezet konfigurálásához és a különböző programok indításához a kívánt környezeti változókkal.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
env [opciók] [argumentumok]
```

## Gyakori opciók
- `-i`: Törli az összes környezeti változót, így csak az újonnan megadott változók érvényesülnek.
- `-u`: Töröl egy adott környezeti változót a futtatás előtt.
- `-0`: A kimenetet null karakterrel választja el, hasznos lehet a fájlnevek kezelésénél.

## Gyakori példák

1. **Környezeti változók megjelenítése**
   ```bash
   env
   ```

2. **Új környezeti változó beállítása és program futtatása**
   ```bash
   env MY_VAR=value ./my_program
   ```

3. **Környezet törlése és új változókkal való futtatás**
   ```bash
   env -i MY_VAR=value ./my_program
   ```

4. **Egy adott környezeti változó törlése**
   ```bash
   env -u MY_VAR ./my_program
   ```

## Tippek
- Használja az `env` parancsot a szkriptek elején, hogy biztosítsa a szükséges környezeti változók beállítását.
- Ellenőrizze a környezeti változók értékeit az `env` parancs segítségével, mielőtt programokat futtatna, hogy elkerülje a váratlan viselkedést.
- A `-0` opciót használja, ha fájlnevekkel dolgozik, amelyek tartalmazhatnak szóközöket vagy speciális karaktereket.