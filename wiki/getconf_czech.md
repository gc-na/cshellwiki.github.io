# [Linux] Bash getconf použití: Získání systémových konfiguračních hodnot

## Přehled
Příkaz `getconf` se používá k získání systémových konfiguračních hodnot a informací o systému. Umožňuje uživatelům zjistit různé parametry operačního systému, jako jsou velikosti bloků, limity a další specifikace.

## Použití
Základní syntaxe příkazu je následující:

```
getconf [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechny dostupné konfigurační hodnoty.
- `NAME`: Název konkrétní konfigurační hodnoty, kterou chcete získat (např. `PAGE_SIZE`).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `getconf`:

1. Získání velikosti stránky v bajtech:
   ```bash
   getconf PAGE_SIZE
   ```

2. Získání maximální velikosti souboru:
   ```bash
   getconf _PC_MAX_INPUT
   ```

3. Zobrazení všech dostupných konfiguračních hodnot:
   ```bash
   getconf -a
   ```

4. Získání velikosti bloku souborového systému:
   ```bash
   getconf BLOCK_SIZE
   ```

## Tipy
- Používejte možnost `-a`, pokud chcete rychle zjistit všechny dostupné konfigurační hodnoty a jejich aktuální nastavení.
- Pokud neznáte přesný název konfigurační hodnoty, můžete se podívat na dokumentaci nebo použít příkaz `man getconf` pro více informací.
- Příkaz `getconf` je užitečný při skriptování, kdy potřebujete dynamicky získat systémové parametry.