# [Linux] Bash comm příkaz: porovnání dvou souborů

## Přehled
Příkaz `comm` slouží k porovnání dvou tříděných souborů a zobrazuje řádky, které se nacházejí v jednom nebo obou souborech. Tento příkaz je užitečný pro analýzu rozdílů mezi dvěma soubory a pro zjištění, které řádky jsou unikátní nebo společné.

## Použití
Základní syntaxe příkazu je následující:

```bash
comm [možnosti] [soubor1] [soubor2]
```

## Běžné možnosti
- `-1`: Potlačí výstup řádků, které se nacházejí pouze v prvním souboru.
- `-2`: Potlačí výstup řádků, které se nacházejí pouze ve druhém souboru.
- `-3`: Potlačí výstup řádků, které se nacházejí v obou souborech.
- `--nocheck-order`: Umožňuje porovnávat soubory, které nejsou seřazené.

## Běžné příklady
1. Základní porovnání dvou souborů:
   ```bash
   comm soubor1.txt soubor2.txt
   ```

2. Zobrazení pouze řádků, které se nacházejí pouze v prvním souboru:
   ```bash
   comm -13 soubor1.txt soubor2.txt
   ```

3. Zobrazení pouze řádků, které se nacházejí pouze ve druhém souboru:
   ```bash
   comm -12 soubor1.txt soubor2.txt
   ```

4. Porovnání dvou nesetříděných souborů:
   ```bash
   comm --nocheck-order soubor1.txt soubor2.txt
   ```

## Tipy
- Ujistěte se, že soubory, které porovnáváte, jsou seřazené, jinak může být výstup nepřesný.
- Používejte možnosti `-1`, `-2` a `-3` pro filtrování výstupu podle vašich potřeb.
- Pokud potřebujete porovnat více než dva soubory, zvažte použití příkazu `diff`, který může poskytnout podrobnější analýzu rozdílů.