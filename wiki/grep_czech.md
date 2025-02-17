# [Linux] Bash grep použití: Hledání textu v souborech

## Přehled
Příkaz `grep` slouží k vyhledávání textových řetězců v souborech. Umožňuje uživatelům rychle najít konkrétní vzory nebo slova v textu, což je užitečné při analýze logů, skriptů a dalších textových dat.

## Použití
Základní syntaxe příkazu `grep` je následující:

```
grep [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Ignoruje velikost písmen při vyhledávání.
- `-v`: Zobrazí řádky, které neodpovídají vzoru.
- `-r`: Prohledává adresáře rekurzivně.
- `-n`: Zobrazí čísla řádků, kde se vzor nachází.
- `-l`: Zobrazí pouze názvy souborů, které obsahují vzor.

## Běžné příklady
1. Hledání konkrétního slova v souboru:
   ```bash
   grep "slovo" soubor.txt
   ```

2. Hledání slova bez ohledu na velikost písmen:
   ```bash
   grep -i "slovo" soubor.txt
   ```

3. Hledání vzoru ve všech souborech v adresáři:
   ```bash
   grep "slovo" *
   ```

4. Zobrazení čísel řádků, kde se vzor nachází:
   ```bash
   grep -n "slovo" soubor.txt
   ```

5. Hledání vzoru rekurzivně v adresáři:
   ```bash
   grep -r "slovo" /cesta/k/adresáři
   ```

## Tipy
- Používejte `-i`, pokud chcete ignorovat velikost písmen, což může být užitečné při vyhledávání běžných výrazů.
- Kombinujte `grep` s dalšími příkazy, jako je `pipe` (`|`), pro efektivnější zpracování dat.
- Pokud hledáte více vzorů, můžete použít `-e` pro každý vzor:
  ```bash
  grep -e "slovo1" -e "slovo2" soubor.txt
  ```