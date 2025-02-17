# [Linux] Bash @ @: Zobrazí aktuální pracovní adresář

## Přehled
Příkaz `pwd` (print working directory) slouží k zobrazení aktuálního pracovního adresáře v terminálu. Tento příkaz je užitečný pro ověření, kde se nacházíte v hierarchii souborového systému.

## Použití
Základní syntaxe příkazu je následující:

```bash
pwd [options]
```

## Běžné možnosti
- `-L`: Zobrazí logickou cestu k aktuálnímu adresáři (výchozí).
- `-P`: Zobrazí fyzickou cestu k aktuálnímu adresáři, což může být užitečné, pokud používáte symbolické odkazy.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `pwd`:

1. Základní použití pro zobrazení aktuálního adresáře:
   ```bash
   pwd
   ```

2. Zobrazení fyzické cesty k aktuálnímu adresáři:
   ```bash
   pwd -P
   ```

3. Zobrazení logické cesty k aktuálnímu adresáři (pokud je to potřeba):
   ```bash
   pwd -L
   ```

## Tipy
- Používejte `pwd` před prováděním operací, které mění adresáře, abyste se ujistili, kde se nacházíte.
- V kombinaci s jinými příkazy, jako je `cd`, může být užitečné pro skripty, které potřebují znát aktuální umístění.