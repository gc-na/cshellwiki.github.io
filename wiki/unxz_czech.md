# [Linux] Bash unxz použití: Rozbalení souborů ve formátu .xz

## Přehled
Příkaz `unxz` slouží k rozbalení souborů komprimovaných pomocí algoritmu LZMA, které mají příponu `.xz`. Tento příkaz je užitečný pro dekompresi souborů, které byly zmenšeny pro úsporu místa na disku.

## Použití
Základní syntaxe příkazu je následující:

```
unxz [možnosti] [argumenty]
```

## Běžné možnosti
- `-k`, `--keep`: Zachová původní soubor po dekompresi.
- `-f`, `--force`: Přepíše existující soubory bez potvrzení.
- `-v`, `--verbose`: Zobrazí podrobnosti o procesu dekomprese.

## Běžné příklady
1. **Základní dekomprese souboru**:
   ```bash
   unxz soubor.xz
   ```

2. **Zachování původního souboru**:
   ```bash
   unxz -k soubor.xz
   ```

3. **Přepsání existujícího souboru**:
   ```bash
   unxz -f soubor.xz
   ```

4. **Zobrazení podrobností o dekompresi**:
   ```bash
   unxz -v soubor.xz
   ```

## Tipy
- Před použitím `unxz` se ujistěte, že máte dostatek volného místa na disku pro rozbalený soubor.
- Pokud často pracujete s komprimovanými soubory, zvažte použití možnosti `-k`, abyste neztratili původní soubory.
- Používejte možnost `-v`, pokud potřebujete sledovat pokrok dekompresního procesu.