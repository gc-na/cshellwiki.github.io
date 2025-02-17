# [Linux] Bash id použití: Zobrazí informace o uživatelském účtu

## Přehled
Příkaz `id` slouží k zobrazení informací o aktuálním uživatelském účtu a skupinách, do kterých tento účet patří. Tento příkaz je užitečný pro správu uživatelských oprávnění a pro diagnostiku problémů s přístupem.

## Použití
Základní syntaxe příkazu `id` je následující:

```bash
id [možnosti] [uživatelské_jméno]
```

## Běžné možnosti
- `-u`: Zobrazí pouze ID aktuálního uživatele.
- `-g`: Zobrazí pouze ID primární skupiny aktuálního uživatele.
- `-G`: Zobrazí všechny skupiny, do kterých uživatel patří.
- `-n`: Zobrazí jména místo čísel ID.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `id`:

1. Zobrazení informací o aktuálním uživatelském účtu:
   ```bash
   id
   ```

2. Zobrazení pouze ID aktuálního uživatele:
   ```bash
   id -u
   ```

3. Zobrazení ID primární skupiny aktuálního uživatele:
   ```bash
   id -g
   ```

4. Zobrazení všech skupin, do kterých uživatel patří:
   ```bash
   id -G
   ```

5. Zobrazení jména aktuálního uživatele místo ID:
   ```bash
   id -n -u
   ```

## Tipy
- Používejte příkaz `id` bez argumentů pro rychlé zjištění informací o vašem účtu.
- Kombinujte možnosti pro získání podrobnějších informací, například `id -Gn` pro zobrazení názvů všech skupin.
- Pokud potřebujete zjistit informace o jiném uživatelském účtu, jednoduše přidejte uživatelské jméno jako argument.