# [Linux] Bash pvs použití: Zobrazí informace o svazcích

## Přehled
Příkaz `pvs` slouží k zobrazení informací o svazcích v systému správy svazků LVM (Logical Volume Manager). Umožňuje uživatelům rychle získat přehled o dostupných svazcích a jejich vlastnostech.

## Použití
Základní syntaxe příkazu `pvs` je následující:

```bash
pvs [možnosti] [argumenty]
```

## Běžné možnosti
- `-o, --options <seznam>`: Určuje, které sloupce se mají zobrazit.
- `-f, --full`: Zobrazí všechny informace o svazcích, včetně skrytých.
- `-a, --all`: Zobrazí všechny svazky, včetně neaktivních.
- `--units <jednotky>`: Umožňuje specifikovat jednotky pro výstup (např. MB, GB).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `pvs`:

1. Základní zobrazení informací o svazcích:
   ```bash
   pvs
   ```

2. Zobrazení podrobných informací o svazcích:
   ```bash
   pvs -f
   ```

3. Zobrazení všech svazků, včetně neaktivních:
   ```bash
   pvs -a
   ```

4. Zobrazení specifických informací o svazcích:
   ```bash
   pvs -o +pv_size
   ```

5. Zobrazení informací o svazcích v gigabytech:
   ```bash
   pvs --units g
   ```

## Tipy
- Používejte možnost `-o` pro zobrazení pouze těch informací, které jsou pro vás relevantní.
- Při práci s LVM je dobré mít na paměti, že příkaz `pvs` můžete kombinovat s dalšími příkazy, jako jsou `lvdisplay` nebo `vgdisplay`, pro komplexnější správu svazků.
- Pravidelně kontrolujte stav svazků, abyste předešli problémům s úložištěm.