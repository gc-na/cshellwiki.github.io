# [Linux] Bash pacman použití: Správa balíčků v systému Arch Linux

## Přehled
Příkaz `pacman` je správce balíčků pro distribuce založené na Arch Linuxu. Umožňuje uživatelům instalovat, aktualizovat a odstraňovat software z jejich systému. `pacman` spravuje balíčky ve formátu `.pkg.tar.zst` a zajišťuje závislosti mezi nimi.

## Použití
Základní syntaxe příkazu `pacman` je následující:

```bash
pacman [možnosti] [argumenty]
```

## Běžné možnosti
- `-S`: Instalace balíčku.
- `-R`: Odebrání balíčku.
- `-U`: Instalace balíčku z lokálního souboru.
- `-Sy`: Aktualizace databáze balíčků.
- `-Su`: Aktualizace všech nainstalovaných balíčků.
- `-Q`: Dotaz na informace o nainstalovaných balíčcích.

## Běžné příklady
1. **Instalace balíčku**:
   ```bash
   pacman -S název_balíčku
   ```

2. **Odebrání balíčku**:
   ```bash
   pacman -R název_balíčku
   ```

3. **Aktualizace databáze balíčků**:
   ```bash
   pacman -Sy
   ```

4. **Aktualizace všech nainstalovaných balíčků**:
   ```bash
   pacman -Su
   ```

5. **Instalace balíčku z lokálního souboru**:
   ```bash
   pacman -U /cesta/k/balíčku.pkg.tar.zst
   ```

6. **Získání informací o nainstalovaném balíčku**:
   ```bash
   pacman -Q název_balíčku
   ```

## Tipy
- Před instalací nového balíčku je dobré vždy aktualizovat databázi balíčků pomocí `pacman -Sy`.
- Používejte `pacman -Rns` pro odebrání balíčku včetně jeho závislostí, které již nejsou potřeba.
- Pro zajištění stability systému pravidelně aktualizujte všechny nainstalované balíčky pomocí `pacman -Su`.