# [Linux] Bash lvextend použití: Rozšíření logických svazků

## Přehled
Příkaz `lvextend` slouží k rozšíření velikosti logických svazků v systému Linux. Umožňuje uživatelům zvýšit kapacitu svazku, což je užitečné, když je potřeba více místa pro ukládání dat.

## Použití
Základní syntaxe příkazu je následující:

```bash
lvextend [možnosti] [argumenty]
```

## Běžné možnosti
- `-L, --size`: Určuje novou velikost logického svazku.
- `-l, --extents`: Umožňuje specifikovat počet rozšíření, o které se má svazek zvětšit.
- `-r, --resizefs`: Automaticky rozšiřuje souborový systém na novou velikost logického svazku.
- `-n, --name`: Umožňuje změnit název logického svazku.

## Běžné příklady
1. **Zvětšení logického svazku na konkrétní velikost**:
   ```bash
   lvextend -L +10G /dev/vg01/lv01
   ```

2. **Zvětšení logického svazku o určitý počet rozšíření**:
   ```bash
   lvextend -l +100 /dev/vg01/lv01
   ```

3. **Zvětšení logického svazku a automatické rozšíření souborového systému**:
   ```bash
   lvextend -r -L +5G /dev/vg01/lv01
   ```

4. **Změna názvu logického svazku**:
   ```bash
   lvextend -n novy_nazev /dev/vg01/stary_nazev
   ```

## Tipy
- Před rozšířením logického svazku se ujistěte, že máte dostatek volného místa ve skupině svazků.
- Vždy je dobré provést zálohu dat před provedením operací, které mění velikost svazků.
- Použití možnosti `-r` je doporučeno, pokud chcete, aby se souborový systém automaticky přizpůsobil nové velikosti logického svazku.