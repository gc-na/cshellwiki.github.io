# [Linux] Bash chgrp použití: Změna skupiny souborů

## Přehled
Příkaz `chgrp` slouží ke změně skupiny vlastnictví souboru nebo adresáře. Umožňuje uživatelům přiřadit soubory a adresáře k jiné skupině, což může být užitečné při správě oprávnění a přístupu k souborům.

## Použití
Základní syntaxe příkazu `chgrp` je následující:

```bash
chgrp [možnosti] [argumenty]
```

## Běžné možnosti
- `-R`: Rekurzivně změní skupinu pro všechny soubory a podadresáře v daném adresáři.
- `-v`: Zobrazí podrobnosti o změnách, které byly provedeny.
- `-c`: Zobrazí pouze změny, které byly skutečně provedeny.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `chgrp`:

1. Změna skupiny souboru `soubor.txt` na `novaskupina`:
   ```bash
   chgrp novaskupina soubor.txt
   ```

2. Rekurzivní změna skupiny pro všechny soubory v adresáři `moje_adresar`:
   ```bash
   chgrp -R novaskupina moje_adresar
   ```

3. Zobrazení změn při změně skupiny souboru `dokument.pdf`:
   ```bash
   chgrp -v novaskupina dokument.pdf
   ```

4. Zobrazení pouze skutečných změn při změně skupiny pro více souborů:
   ```bash
   chgrp -c novaskupina soubor1.txt soubor2.txt
   ```

## Tipy
- Ujistěte se, že máte potřebná oprávnění pro změnu skupiny souboru nebo adresáře.
- Před použitím příkazu `chgrp` je dobré zkontrolovat aktuální skupinu pomocí příkazu `ls -l`.
- Používejte rekurzivní možnost `-R` opatrně, abyste nezměnili skupinu souborů, které byste nechtěli ovlivnit.