# [Linux] Bash ls použití: Zobrazí obsah adresáře

## Přehled
Příkaz `ls` slouží k zobrazení obsahu adresáře. Umožňuje uživatelům rychle zjistit, jaké soubory a složky se nacházejí v aktuálním nebo zvoleném adresáři.

## Použití
Základní syntaxe příkazu `ls` je následující:
```bash
ls [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Zobrazí podrobný seznam souborů a složek včetně oprávnění, vlastníka, velikosti a data poslední změny.
- `-a`: Zobrazí všechny soubory, včetně skrytých (ty, které začínají tečkou).
- `-h`: Zobrazí velikosti souborů v lidsky čitelném formátu (např. KB, MB).
- `-R`: Rekurzivně zobrazí obsah všech podsložek.
- `-t`: Seřadí soubory podle data poslední změny, od nejnovějších po nejstarší.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `ls`:

1. Základní zobrazení obsahu aktuálního adresáře:
   ```bash
   ls
   ```

2. Zobrazení obsahu s podrobnými informacemi:
   ```bash
   ls -l
   ```

3. Zobrazení všech souborů včetně skrytých:
   ```bash
   ls -a
   ```

4. Zobrazení obsahu adresáře s lidsky čitelnými velikostmi:
   ```bash
   ls -lh
   ```

5. Rekurzivní zobrazení obsahu adresáře:
   ```bash
   ls -R
   ```

6. Seřazení souborů podle data poslední změny:
   ```bash
   ls -lt
   ```

## Tipy
- Používejte `ls -la` pro rychlý přehled o všech souborech, včetně skrytých, a jejich podrobných informacích.
- Kombinujte možnosti pro přizpůsobení výstupu podle potřeby, například `ls -lhR` pro podrobný rekurzivní výpis.
- Pokud často používáte `ls`, zvažte vytvoření aliasu pro oblíbené možnosti v souboru `.bashrc` pro rychlejší přístup.