# [Linux] Bash cd použití: Přechod mezi adresáři

## Přehled
Příkaz `cd` (change directory) slouží k přechodu mezi adresáři v systému souborů. Umožňuje uživatelům změnit aktuální pracovní adresář, což je nezbytné pro efektivní navigaci a správu souborů v terminálu.

## Použití
Základní syntaxe příkazu `cd` je následující:

```bash
cd [možnosti] [argumenty]
```

## Běžné možnosti
- `-` : Přepne se zpět do předchozího adresáře.
- `~` : Přepne se do domovského adresáře aktuálního uživatele.
- `..` : Přepne se do nadřazeného adresáře.

## Běžné příklady
1. Přechod do domovského adresáře:
   ```bash
   cd ~
   ```

2. Přechod do nadřazeného adresáře:
   ```bash
   cd ..
   ```

3. Přechod do konkrétního adresáře (např. do adresáře "Dokumenty"):
   ```bash
   cd Dokumenty
   ```

4. Přepnutí zpět do předchozího adresáře:
   ```bash
   cd -
   ```

5. Přechod do absolutní cesty:
   ```bash
   cd /usr/local/bin
   ```

## Tipy
- Používejte `cd -` pro rychlé přepínání mezi dvěma adresáři.
- Pokud potřebujete zjistit, kde se právě nacházíte, použijte příkaz `pwd` (print working directory).
- Pro zjednodušení můžete používat zkrácené názvy adresářů, pokud se nacházíte v jejich nadřazených adresářích.