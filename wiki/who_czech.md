# [Linux] Bash who použití: Zobrazí přihlášené uživatele

## Přehled
Příkaz `who` slouží k zobrazení seznamu uživatelů, kteří jsou aktuálně přihlášeni do systému. Tento příkaz poskytuje informace o uživatelských účtech, jako je název uživatele, terminál, čas přihlášení a další relevantní údaje.

## Použití
Základní syntaxe příkazu `who` je následující:

```
who [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechny dostupné informace o uživatelích.
- `-b`: Zobrazí čas posledního restartu systému.
- `-q`: Zobrazí pouze seznam uživatelů a počet přihlášených uživatelů.
- `--help`: Zobrazí nápovědu k použití příkazu.

## Běžné příklady
1. Základní použití pro zobrazení přihlášených uživatelů:
   ```bash
   who
   ```

2. Zobrazení všech dostupných informací o uživatelích:
   ```bash
   who -a
   ```

3. Zobrazení času posledního restartu systému:
   ```bash
   who -b
   ```

4. Zobrazení pouze seznamu uživatelů a jejich počtu:
   ```bash
   who -q
   ```

## Tipy
- Používejte `who` v kombinaci s dalšími příkazy, jako je `grep`, pro filtrování specifických uživatelů.
- Pokud potřebujete sledovat aktivitu uživatelů v reálném čase, můžete použít příkaz `watch` s `who`:
  ```bash
  watch who
  ```
- Pro zobrazení podrobnějších informací o uživatelských relacích můžete kombinovat `who` s příkazem `last`.