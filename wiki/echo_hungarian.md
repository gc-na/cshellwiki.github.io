# [Linux] Bash echo használata: Szöveg kiírása a terminálra

## Áttekintés
Az `echo` parancs a Bash környezetben arra szolgál, hogy szöveget vagy változók értékét írja ki a terminálra. Ez egy alapvető eszköz a parancssori kimenet kezelésére és a szkriptekben való használatra.

## Használat
A `echo` parancs alapvető szintaxisa a következő:

```bash
echo [opciók] [argumentumok]
```

## Gyakori Opciók
- `-n`: Ne írjon ki új sort a végén.
- `-e`: Engedélyezi az escape karakterek használatát, mint például `\n` (új sor) és `\t` (tabulátor).
- `-E`: Az escape karakterek letiltása (ez az alapértelmezett viselkedés).

## Gyakori Példák
1. Egyszerű szöveg kiírása:
   ```bash
   echo "Helló, világ!"
   ```

2. Új sor nélkül:
   ```bash
   echo -n "Ez egy sor, "
   echo "ez pedig a folytatása."
   ```

3. Escape karakterek használata:
   ```bash
   echo -e "Első sor\nMásodik sor"
   ```

4. Változó értékének kiírása:
   ```bash
   név="János"
   echo "Üdvözöllek, $név!"
   ```

5. Szöveg kiírása tabulátorral:
   ```bash
   echo -e "Első oszlop\tMásodik oszlop"
   ```

## Tippek
- Használj `-n` opciót, ha nem szeretnéd, hogy a kimenet új sorral záruljon.
- Az `-e` opcióval könnyen formázhatod a kimenetet, például új sorokat és tabulátorokat adhatsz hozzá.
- Változók kiírásakor mindig használj idézőjeleket, hogy elkerüld a nem kívánt kimenetet vagy hibákat.