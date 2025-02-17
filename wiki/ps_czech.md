# [Linux] Bash ps použití: Zobrazení běžících procesů

## Přehled
Příkaz `ps` slouží k zobrazení aktuálně běžících procesů na systému. Umožňuje uživatelům získat informace o procesech, jako jsou jejich ID, stav, využití CPU a paměti, a další důležité detaily.

## Použití
Základní syntaxe příkazu `ps` je následující:

```bash
ps [možnosti] [argumenty]
```

## Běžné možnosti
- `-e` nebo `-A`: Zobrazí všechny procesy.
- `-f`: Zobrazí procesy v úplném formátu, včetně informací o rodičovských procesech.
- `-u [uživatel]`: Zobrazí procesy patřící konkrétnímu uživateli.
- `-aux`: Zobrazí všechny procesy s podrobnými informacemi.
- `--sort`: Umožňuje seřadit výstup podle specifikovaných kritérií.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `ps`:

1. Zobrazení všech běžících procesů:
   ```bash
   ps -e
   ```

2. Zobrazení procesů v úplném formátu:
   ```bash
   ps -f
   ```

3. Zobrazení procesů konkrétního uživatele:
   ```bash
   ps -u username
   ```

4. Zobrazení všech procesů s podrobnými informacemi:
   ```bash
   ps aux
   ```

5. Seřazení procesů podle využití paměti:
   ```bash
   ps aux --sort=-%mem
   ```

## Tipy
- Používejte `ps aux` pro rychlý přehled o všech procesech běžících na systému.
- Kombinujte `ps` s příkazem `grep` pro filtrování specifických procesů. Například:
  ```bash
  ps aux | grep firefox
  ```
- Pro sledování procesů v reálném čase můžete použít příkaz `top`, který poskytuje dynamický pohled na běžící procesy.