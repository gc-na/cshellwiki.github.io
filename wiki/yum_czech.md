# [Linux] Bash yum použití: Správa balíčků v systému

## Přehled
Příkaz `yum` (Yellowdog Updater, Modified) je nástroj pro správu balíčků v distribucích Linuxu založených na RPM, jako je CentOS a Fedora. Umožňuje uživatelům instalovat, aktualizovat a odstraňovat software z jejich systémů.

## Použití
Základní syntaxe příkazu `yum` je následující:

```
yum [možnosti] [argumenty]
```

## Běžné možnosti
- `install`: Nainstaluje balíček.
- `remove`: Odstraní balíček.
- `update`: Aktualizuje nainstalované balíčky na nejnovější verzi.
- `search`: Hledá balíčky podle názvu nebo popisu.
- `info`: Zobrazí informace o balíčku.

## Běžné příklady
### Instalace balíčku
Chcete-li nainstalovat balíček, použijte:
```bash
yum install název_balíčku
```

### Odstranění balíčku
Pro odstranění balíčku použijte:
```bash
yum remove název_balíčku
```

### Aktualizace balíčků
Pro aktualizaci všech nainstalovaných balíčků použijte:
```bash
yum update
```

### Hledání balíčku
Pokud chcete najít balíček podle názvu, použijte:
```bash
yum search klíčové_slovo
```

### Získání informací o balíčku
Pro zobrazení informací o konkrétním balíčku použijte:
```bash
yum info název_balíčku
```

## Tipy
- Před provedením aktualizace doporučujeme vytvořit zálohu důležitých dat.
- Používejte `yum clean all`, abyste uvolnili místo na disku odstraněním mezipaměti.
- Pravidelně kontrolujte dostupné aktualizace, aby váš systém zůstal zabezpečený a aktuální.