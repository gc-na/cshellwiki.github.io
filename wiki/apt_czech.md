# [Linux] Bash apt použití: Správa balíčků v systému

## Přehled
Příkaz `apt` je nástroj pro správu balíčků v distribucích Linuxu založených na Debianu. Umožňuje uživatelům instalovat, aktualizovat a odstraňovat software z příkazového řádku.

## Použití
Základní syntaxe příkazu `apt` je následující:

```
apt [možnosti] [argumenty]
```

## Běžné možnosti
- `install`: Nainstaluje zadaný balíček.
- `remove`: Odebere zadaný balíček.
- `update`: Aktualizuje seznam dostupných balíčků.
- `upgrade`: Aktualizuje nainstalované balíčky na nejnovější verze.
- `search`: Hledá balíčky podle názvu nebo popisu.

## Běžné příklady
1. **Aktualizace seznamu balíčků:**
   ```bash
   sudo apt update
   ```

2. **Instalace balíčku:**
   ```bash
   sudo apt install název_balíčku
   ```

3. **Odstranění balíčku:**
   ```bash
   sudo apt remove název_balíčku
   ```

4. **Aktualizace všech nainstalovaných balíčků:**
   ```bash
   sudo apt upgrade
   ```

5. **Hledání balíčku:**
   ```bash
   apt search název_balíčku
   ```

## Tipy
- Vždy spusťte `sudo apt update` před instalací nebo aktualizací balíčků, abyste zajistili, že máte nejnovější informace o dostupných verzích.
- Používejte `apt autoremove` k odstranění nepotřebných balíčků, které byly nainstalovány jako závislosti.
- Při instalaci více balíčků je můžete zadat všechny najednou, oddělené mezerou, například: `sudo apt install balíček1 balíček2`.