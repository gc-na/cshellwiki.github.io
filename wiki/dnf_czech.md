# [Linux] Bash dnf Použití: Správa balíčků v distribucích založených na RPM

## Přehled
Příkaz `dnf` (Dandified YUM) je moderní nástroj pro správu balíčků v distribucích Linuxu, které používají RPM (Red Hat Package Manager). Umožňuje uživatelům instalovat, aktualizovat, odinstalovat a spravovat software na jejich systémech.

## Použití
Základní syntaxe příkazu `dnf` je následující:

```bash
dnf [možnosti] [argumenty]
```

## Běžné možnosti
- `install`: Nainstaluje balíček.
- `remove`: Odinstaluje balíček.
- `update`: Aktualizuje nainstalované balíčky na nejnovější verzi.
- `search`: Hledá balíčky podle názvu nebo popisu.
- `info`: Zobrazí informace o balíčku.
- `list`: Zobrazí seznam nainstalovaných nebo dostupných balíčků.

## Běžné příklady
1. **Instalace balíčku:**
   ```bash
   dnf install název_balíčku
   ```

2. **Odinstalace balíčku:**
   ```bash
   dnf remove název_balíčku
   ```

3. **Aktualizace všech nainstalovaných balíčků:**
   ```bash
   dnf update
   ```

4. **Hledání balíčku:**
   ```bash
   dnf search název_balíčku
   ```

5. **Zobrazení informací o balíčku:**
   ```bash
   dnf info název_balíčku
   ```

6. **Zobrazení seznamu nainstalovaných balíčků:**
   ```bash
   dnf list installed
   ```

## Tipy
- Před provedením aktualizace je dobré provést zálohu důležitých dat.
- Používejte `dnf clean all` pro vyčištění mezipaměti a uvolnění místa na disku.
- Pro zobrazení podrobnějších informací o příkazu můžete použít `dnf --help`.