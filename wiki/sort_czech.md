# [Linux] Bash sort použití: Řazení textových řetězců

## Přehled
Příkaz `sort` slouží k řazení řádků textových souborů nebo standardního vstupu. Může se použít k uspořádání dat podle abecedy, čísel nebo jiných kritérií.

## Použití
Základní syntaxe příkazu je následující:

```bash
sort [možnosti] [argumenty]
```

## Běžné možnosti
- `-n`: Řadí čísla podle jejich hodnoty.
- `-r`: Řadí v opačném pořadí (sestupně).
- `-k`: Určuje klíč pro řazení (např. `-k2` pro řazení podle druhého sloupce).
- `-u`: Odstraní duplicitní řádky.
- `-o`: Uloží výstup do souboru (např. `-o výstup.txt`).

## Běžné příklady
1. Řazení souboru `data.txt` podle abecedy:
   ```bash
   sort data.txt
   ```

2. Řazení čísel v souboru `numbers.txt`:
   ```bash
   sort -n numbers.txt
   ```

3. Řazení v opačném pořadí:
   ```bash
   sort -r data.txt
   ```

4. Řazení podle druhého sloupce v souboru `data.txt`:
   ```bash
   sort -k2 data.txt
   ```

5. Uložení seřazeného výstupu do nového souboru:
   ```bash
   sort data.txt -o sorted_data.txt
   ```

## Tipy
- Používejte možnost `-u`, pokud chcete rychle odstranit duplicitní řádky.
- Kombinujte možnosti pro složitější řazení, například `sort -n -r` pro řazení čísel v sestupném pořadí.
- Pokud pracujete s velkými soubory, zvažte použití `sort` s parametrem `--parallel`, který umožňuje paralelní zpracování.