# [Linux] Bash chage použití: Správa expirace hesel uživatelů

## Overview
Příkaz `chage` slouží k úpravě informací o expiraci hesel pro uživatelské účty v systému. Umožňuje administrátorům nastavit, jak dlouho mohou uživatelé používat své heslo, a kdy musí heslo změnit.

## Usage
Základní syntaxe příkazu `chage` je následující:

```bash
chage [options] [arguments]
```

## Common Options
- `-l, --list`: Zobrazí informace o expiraci hesla pro daného uživatele.
- `-m, --mindays`: Nastaví minimální počet dní mezi změnami hesla.
- `-M, --maxdays`: Nastaví maximální počet dní, po kterých musí být heslo změněno.
- `-I, --inactive`: Nastaví počet dní po expiraci hesla, během kterých může uživatel stále přihlásit.
- `-E, --expire`: Nastaví datum, kdy bude účet uzavřen.

## Common Examples
Zde je několik praktických příkladů použití příkazu `chage`:

1. Zobrazení informací o expiraci hesla pro uživatele `janek`:

    ```bash
    chage -l janek
    ```

2. Nastavení minimálního počtu dní mezi změnami hesla na 5 dní pro uživatele `petr`:

    ```bash
    chage -m 5 petr
    ```

3. Nastavení maximálního počtu dní pro změnu hesla na 30 dní pro uživatele `eva`:

    ```bash
    chage -M 30 eva
    ```

4. Nastavení neaktivního období na 15 dní po expiraci hesla pro uživatele `martin`:

    ```bash
    chage -I 15 martin
    ```

5. Nastavení data expirace účtu pro uživatele `lucie` na 1. ledna 2024:

    ```bash
    chage -E 2024-01-01 lucie
    ```

## Tips
- Před použitím příkazu `chage` se ujistěte, že máte potřebná oprávnění (obvykle jako superuživatel).
- Pravidelně kontrolujte expiraci hesel uživatelů, abyste zajistili bezpečnost systému.
- Používejte příkaz `chage -l` pro rychlé ověření aktuálních nastavení expirace hesel pro uživatele.