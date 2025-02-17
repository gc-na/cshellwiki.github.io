# [Linux] Bash du použití: Zobrazení velikosti souborů a adresářů

## Přehled
Příkaz `du` (disk usage) slouží k zobrazení velikosti souborů a adresářů v systému. Umožňuje uživatelům zjistit, kolik místa jednotlivé soubory a složky zabírají na disku.

## Použití
Základní syntaxe příkazu `du` je následující:

```bash
du [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Zobrazí velikosti v lidsky čitelném formátu (např. KB, MB).
- `-s`: Zobrazí pouze celkovou velikost pro každý argument.
- `-a`: Zobrazí velikosti všech souborů i adresářů.
- `-c`: Zobrazí celkovou velikost na konci výstupu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `du`:

1. Zobrazení velikosti aktuálního adresáře a jeho podadresářů:
   ```bash
   du
   ```

2. Zobrazení velikosti aktuálního adresáře v lidsky čitelném formátu:
   ```bash
   du -h
   ```

3. Zobrazení celkové velikosti konkrétního adresáře:
   ```bash
   du -sh /cesta/k/adresáři
   ```

4. Zobrazení velikosti všech souborů a adresářů v aktuálním adresáři:
   ```bash
   du -a
   ```

5. Zobrazení velikosti adresářů a souborů s celkovým součtem na konci:
   ```bash
   du -ch
   ```

## Tipy
- Používejte možnost `-h`, abyste snadno porozuměli velikostem souborů.
- Pokud chcete zjistit, které složky zabírají nejvíce místa, zkombinujte `du` s příkazem `sort`:
  ```bash
  du -h | sort -hr
  ```
- Pravidelně kontrolujte velikosti adresářů, abyste se ujistili, že máte dostatek místa na disku.