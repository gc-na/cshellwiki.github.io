# [Linux] Bash export használata: Környezeti változók beállítása

## Áttekintés
Az `export` parancs a Bash környezetben lehetővé teszi a környezeti változók beállítását és elérhetővé tételét a gyermek folyamatok számára. Ez hasznos, ha globálisan szeretnénk megosztani változókat a shell és a programok között.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
export [opciók] [változó=érték]
```

## Gyakori opciók
- `-p`: Megjeleníti az összes exportált változót.
- `-n`: Eltávolítja a megadott változót az exportált változók listájából.

## Gyakori példák

1. **Környezet változó létrehozása**
   ```bash
   export MY_VAR="Hello, World!"
   ```

2. **Környezet változó megjelenítése**
   ```bash
   export -p
   ```

3. **Környezet változó eltávolítása az exportált listából**
   ```bash
   export -n MY_VAR
   ```

4. **Környezet változó használata egy parancsban**
   ```bash
   MY_VAR="Hello" export MY_VAR
   echo $MY_VAR
   ```

## Tippek
- Mindig ellenőrizd, hogy a változók megfelelően vannak-e beállítva az `export -p` parancs használatával.
- Használj egyértelmű neveket a változókhoz, hogy könnyen érthető legyen a kód.
- Ne feledd, hogy a változók csak a gyermek folyamatok számára elérhetők, így ha egy új shellt indítasz, a változók nem lesznek elérhetők, hacsak nem exportálod őket újra.