# [Linux] Bash last příkaz: Zobrazí poslední přihlášení uživatelů

## Přehled
Příkaz `last` slouží k zobrazení historie přihlášení uživatelů do systému. Umožňuje uživatelům sledovat, kdo a kdy se přihlásil, což může být užitečné pro audit a bezpečnostní účely.

## Použití
Základní syntaxe příkazu `last` je následující:

```
last [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí hostname posledního přihlášení.
- `-n [číslo]`: Omezí výstup na posledních `číslo` přihlášení.
- `-x`: Zobrazí také informace o ukončených relacích.
- `-R`: Skryje hostname v výstupu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `last`:

1. Zobrazit všechny poslední přihlášení:
   ```bash
   last
   ```

2. Zobrazit posledních 5 přihlášení:
   ```bash
   last -n 5
   ```

3. Zobrazit poslední přihlášení včetně hostname:
   ```bash
   last -a
   ```

4. Zobrazit informace o ukončených relacích:
   ```bash
   last -x
   ```

5. Zobrazit přihlášení pro konkrétního uživatele:
   ```bash
   last username
   ```

## Tipy
- Používejte `last -n` pro rychlé zúžení výstupu, pokud hledáte konkrétní informace.
- Kombinujte možnosti, jako je `last -a -n 10`, pro zobrazení posledních 10 přihlášení včetně hostname.
- Pravidelně kontrolujte historii přihlášení, abyste zajistili bezpečnost vašeho systému.