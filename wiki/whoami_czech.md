# [Linux] Bash whoami použití: Zjistí aktuálního uživatele

## Přehled
Příkaz `whoami` slouží k zobrazení uživatelského jména aktuálně přihlášeného uživatele v systému. Je to užitečný nástroj pro ověření identity uživatele, zejména při práci s více uživatelskými účty nebo při administraci systému.

## Použití
Základní syntaxe příkazu je následující:

```
whoami [možnosti] [argumenty]
```

## Běžné možnosti
- `--help`: Zobrazí nápovědu k příkazu `whoami`.
- `--version`: Zobrazí verzi příkazu `whoami`.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `whoami`:

1. Zobrazení aktuálního uživatelského jména:
   ```bash
   whoami
   ```

2. Zobrazení nápovědy k příkazu:
   ```bash
   whoami --help
   ```

3. Zobrazení verze příkazu:
   ```bash
   whoami --version
   ```

## Tipy
- Používejte příkaz `whoami` v skriptech pro ověření, zda skript běží pod správným uživatelským účtem.
- Pokud potřebujete zjistit ID uživatele, můžete použít příkaz `id`, který poskytuje více informací o uživatelském účtu.
- Příkaz `whoami` je užitečný při práci na vzdálených serverech, kde je důležité vědět, pod jakým uživatelským účtem jste přihlášeni.