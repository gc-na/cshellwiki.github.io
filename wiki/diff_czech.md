# [Linux] Bash diff použití: Porovnání souborů a adresářů

## Přehled
Příkaz `diff` slouží k porovnání obsahu dvou souborů nebo adresářů a zobrazuje rozdíly mezi nimi. Umožňuje uživatelům snadno identifikovat změny, které byly provedeny v textových souborech.

## Použití
Základní syntaxe příkazu `diff` je následující:

```bash
diff [možnosti] [argumenty]
```

## Běžné možnosti
- `-u`: Zobrazí rozdíly v "unified" formátu, který je přehlednější.
- `-i`: Ignoruje rozdíly v malých a velkých písmenech.
- `-w`: Ignoruje bílé znaky (mezery a tabulátory).
- `-r`: Porovná všechny soubory v adresářích rekurzivně.
- `-q`: Zobrazí pouze informace o tom, zda se soubory liší, bez podrobností.

## Běžné příklady
1. Porovnání dvou textových souborů:
   ```bash
   diff soubor1.txt soubor2.txt
   ```

2. Použití "unified" formátu pro přehlednější zobrazení:
   ```bash
   diff -u soubor1.txt soubor2.txt
   ```

3. Ignorování rozdílů v malých a velkých písmenech:
   ```bash
   diff -i soubor1.txt soubor2.txt
   ```

4. Porovnání dvou adresářů rekurzivně:
   ```bash
   diff -r adresar1/ adresar2/
   ```

5. Zobrazení pouze informace o rozdílech bez podrobností:
   ```bash
   diff -q soubor1.txt soubor2.txt
   ```

## Tipy
- Při porovnávání velkých souborů použijte možnost `-u`, abyste získali přehlednější výstup.
- Pokud pracujete s verzemi souborů, zvažte použití `diff` v kombinaci s nástroji pro správu verzí, jako je Git.
- Před provedením porovnání se ujistěte, že máte správné cesty k souborům nebo adresářům, abyste předešli chybám.