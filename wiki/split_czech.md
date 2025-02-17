# [Linux] Bash split použití: Rozdělení souborů na menší části

## Přehled
Příkaz `split` slouží k rozdělení souborů na menší části. Je užitečný, když potřebujete zpracovat velké soubory, které je obtížné spravovat jako celek.

## Použití
Základní syntaxe příkazu je následující:

```
split [možnosti] [argumenty]
```

## Běžné možnosti
- `-l [číslo]`: Rozdělí soubor na části podle počtu řádků.
- `-b [velikost]`: Rozdělí soubor na části podle velikosti (např. `1M` pro 1 megabajt).
- `-d`: Používá číslování s číslicemi místo výchozího písmenkového.
- `--additional-suffix=[sufix]`: Přidá k názvům výstupních souborů specifikovaný sufix.

## Běžné příklady
1. Rozdělení souboru na části po 1000 řádcích:
   ```bash
   split -l 1000 velky_soubor.txt
   ```

2. Rozdělení souboru na části o velikosti 10 megabajtů:
   ```bash
   split -b 10M velky_soubor.txt
   ```

3. Rozdělení souboru s číslováním:
   ```bash
   split -d -l 5000 velky_soubor.txt
   ```

4. Rozdělení souboru a přidání sufixu k názvům výstupních souborů:
   ```bash
   split --additional-suffix=.txt -b 1M velky_soubor.txt cast_
   ```

## Tipy
- Při rozdělování velkých souborů je dobré zvolit vhodnou velikost nebo počet řádků, aby byly výsledné části snadno spravovatelné.
- Zvažte použití možnosti `-d`, pokud potřebujete mít číslované soubory, což může usnadnit jejich pozdější zpracování.
- Nezapomeňte zkontrolovat výstupní soubory, abyste se ujistili, že rozdělení proběhlo podle očekávání.