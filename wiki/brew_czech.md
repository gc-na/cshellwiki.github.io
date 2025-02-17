# [macOS] Bash brew použití: Správa balíčků na macOS

## Přehled
Příkaz `brew` je nástroj pro správu balíčků na operačním systému macOS. Umožňuje uživatelům snadno instalovat, aktualizovat a spravovat software a knihovny přímo z příkazového řádku.

## Použití
Základní syntaxe příkazu `brew` je následující:

```bash
brew [možnosti] [argumenty]
```

## Běžné možnosti
- `install`: Nainstaluje balíček.
- `uninstall`: Odinstaluje balíček.
- `update`: Aktualizuje seznam dostupných balíčků.
- `upgrade`: Aktualizuje nainstalované balíčky na nejnovější verze.
- `list`: Zobrazí seznam nainstalovaných balíčků.

## Běžné příklady
1. **Instalace balíčku**:
   ```bash
   brew install git
   ```
   Tento příkaz nainstaluje systém pro správu verzí Git.

2. **Odinstalace balíčku**:
   ```bash
   brew uninstall git
   ```
   Tento příkaz odstraní Git z vašeho systému.

3. **Aktualizace seznamu balíčků**:
   ```bash
   brew update
   ```
   Tento příkaz aktualizuje seznam dostupných balíčků na vašem systému.

4. **Aktualizace nainstalovaných balíčků**:
   ```bash
   brew upgrade
   ```
   Tento příkaz aktualizuje všechny nainstalované balíčky na nejnovější verze.

5. **Zobrazení seznamu nainstalovaných balíčků**:
   ```bash
   brew list
   ```
   Tento příkaz zobrazí všechny balíčky, které máte nainstalované.

## Tipy
- Před instalací nového balíčku vždy spusťte `brew update`, abyste měli aktuální seznam dostupných verzí.
- Používejte `brew doctor`, abyste zjistili, zda je vaše instalace Homebrew v pořádku a zda neobsahuje chyby.
- Pokud potřebujete konkrétní verzi balíčku, můžete použít `brew search [název]` k nalezení dostupných verzí.