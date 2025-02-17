# [Linux] Bash groups použití: Zobrazení skupin uživatele

## Přehled
Příkaz `groups` slouží k zobrazení skupin, do kterých patří konkrétní uživatel. Tento příkaz je užitečný pro správu oprávnění a pro pochopení, jaké skupiny uživatel má na systému.

## Použití
Základní syntaxe příkazu je následující:

```bash
groups [možnosti] [uživatel]
```

## Běžné možnosti
- `-h`, `--help`: Zobrazí nápovědu k příkazu.
- `-q`, `--quiet`: Zobrazí pouze názvy skupin, bez dalších informací.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `groups`:

1. Zobrazení skupin pro aktuálního uživatele:
    ```bash
    groups
    ```

2. Zobrazení skupin pro konkrétního uživatele (např. uživatel `jan`):
    ```bash
    groups jan
    ```

3. Zobrazení skupin pro více uživatelů (např. uživatelé `jan` a `petr`):
    ```bash
    groups jan petr
    ```

4. Zobrazení skupin s potlačením dalších informací:
    ```bash
    groups -q jan
    ```

## Tipy
- Používejte příkaz `groups` k rychlému ověření, do jakých skupin patříte, což může být užitečné při nastavování oprávnění.
- Pokud potřebujete zjistit skupiny jiného uživatele, ujistěte se, že máte potřebná oprávnění pro zobrazení těchto informací.
- Příkaz `groups` můžete kombinovat s dalšími příkazy, jako je `grep`, pro filtrování výstupu podle specifických skupin.