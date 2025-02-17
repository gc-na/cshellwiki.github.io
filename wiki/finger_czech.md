# [Linux] Bash finger použití: Zobrazí informace o uživatelských účtech

## Přehled
Příkaz `finger` slouží k zobrazení informací o uživatelských účtech na systému. Umožňuje uživatelům získat základní informace, jako jsou jméno, přihlášení, čas posledního přihlášení a další detaily o uživatelích.

## Použití
Základní syntaxe příkazu je následující:
```
finger [options] [arguments]
```

## Běžné možnosti
- `-l`: Zobrazí podrobné informace o uživatelském účtu.
- `-m`: Vyhledává uživatele podle jména, ignoruje velká a malá písmena.
- `-s`: Zobrazí stručné informace o uživatelských účtech (výchozí formát).
- `-p`: Zobrazí informace o uživatelském účtu bez zobrazení posledního přihlášení.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `finger`:

1. Zobrazení informací o všech uživatelích:
   ```bash
   finger
   ```

2. Zobrazení podrobných informací o konkrétním uživateli:
   ```bash
   finger -l username
   ```

3. Vyhledání uživatele bez ohledu na velikost písmen:
   ```bash
   finger -m USERNAME
   ```

4. Zobrazení stručných informací o uživatelských účtech:
   ```bash
   finger -s
   ```

5. Zobrazení informací o uživatelském účtu bez posledního přihlášení:
   ```bash
   finger -p username
   ```

## Tipy
- Používejte `finger` v kombinaci s dalšími příkazy, jako je `grep`, pro filtrování výsledků.
- Pokud potřebujete rychle zjistit, kdo je přihlášen do systému, příkaz `finger` je rychlý a efektivní způsob, jak to udělat.
- Mějte na paměti, že informace zobrazené příkazem `finger` mohou být omezeny nastavením soukromí uživatelů.