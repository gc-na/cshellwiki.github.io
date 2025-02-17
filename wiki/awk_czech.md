# [Linux] Bash awk použití: Zpracování textových dat

## Přehled
Příkaz `awk` je mocný nástroj pro zpracování textových dat a analýzu souborů. Umožňuje uživatelům provádět různé operace na textových řádcích, jako je filtrování, formátování a výpočet. `awk` je často používán pro práci s datovými soubory a logy.

## Použití
Základní syntaxe příkazu `awk` je následující:

```bash
awk [možnosti] [argumenty]
```

## Běžné možnosti
- `-F`: Určuje oddělovač polí (např. `-F,` pro CSV soubory).
- `-v`: Umožňuje definovat proměnné před zpracováním dat.
- `-f`: Umožňuje spustit skript z externího souboru.

## Běžné příklady
1. **Základní použití pro tisk druhého sloupce:**
   ```bash
   awk '{print $2}' soubor.txt
   ```
   Tento příkaz vytiskne druhý sloupec z každého řádku souboru `soubor.txt`.

2. **Použití s oddělovačem:**
   ```bash
   awk -F, '{print $1}' soubor.csv
   ```
   Tento příkaz vytiskne první sloupec z CSV souboru, kde jsou hodnoty odděleny čárkami.

3. **Filtrace řádků podle podmínky:**
   ```bash
   awk '$3 > 50 {print $1, $2}' soubor.txt
   ```
   Tento příkaz vytiskne první a druhý sloupec pouze pro ty řádky, kde je hodnota ve třetím sloupci větší než 50.

4. **Sčítání hodnot ve sloupci:**
   ```bash
   awk '{sum += $1} END {print sum}' soubor.txt
   ```
   Tento příkaz sečte všechny hodnoty v prvním sloupci a vytiskne celkový součet.

## Tipy
- Používejte `-F` pro správné nastavení oddělovače, pokud pracujete s formátovanými daty.
- Vytvářejte skripty `awk` pro složitější analýzy a uložte je do souboru, který můžete spouštět pomocí `awk -f`.
- Experimentujte s proměnnými pomocí `-v`, abyste zjednodušili složité výrazy a podmínky.