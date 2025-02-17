# [Linux] Bash zypper použití: Správa balíčků v openSUSE

## Přehled
Zypper je nástroj pro správu balíčků v distribucích openSUSE a SLE (SUSE Linux Enterprise). Umožňuje uživatelům instalovat, odstraňovat a aktualizovat software, spravovat repozitáře a provádět další úkoly související se správou balíčků.

## Použití
Základní syntaxe příkazu zypper je následující:

```bash
zypper [možnosti] [argumenty]
```

## Běžné možnosti
- `install` - Nainstaluje balíček.
- `remove` - Odstraní balíček.
- `update` - Aktualizuje nainstalované balíčky.
- `search` - Hledá balíčky podle názvu nebo popisu.
- `repos` - Zobrazí seznam dostupných repozitářů.

## Běžné příklady
1. **Instalace balíčku:**
   ```bash
   zypper install název_balíčku
   ```

2. **Odstranění balíčku:**
   ```bash
   zypper remove název_balíčku
   ```

3. **Aktualizace všech nainstalovaných balíčků:**
   ```bash
   zypper update
   ```

4. **Hledání balíčku:**
   ```bash
   zypper search název_balíčku
   ```

5. **Zobrazení seznamu repozitářů:**
   ```bash
   zypper repos
   ```

## Tipy
- Před provedením aktualizace je dobré provést zálohu důležitých dat.
- Používejte `zypper refresh` k aktualizaci informací o repozitářích před instalací nebo aktualizací balíčků.
- Pro zobrazení podrobnějších informací o balíčku použijte `zypper info název_balíčku`.