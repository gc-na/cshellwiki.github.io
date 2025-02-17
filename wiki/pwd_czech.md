# [Linux] Bash pwd použití: Zobrazí aktuální pracovní adresář

## Přehled
Příkaz `pwd` (print working directory) slouží k zobrazení aktuálního pracovního adresáře v terminálu. Tento příkaz je užitečný pro ověření, kde se nacházíte v hierarchii souborového systému.

## Použití
Základní syntaxe příkazu je následující:

```
pwd [možnosti]
```

## Běžné možnosti
- `-L`: Zobrazí logickou cestu k aktuálnímu adresáři (výchozí chování).
- `-P`: Zobrazí fyzickou cestu k aktuálnímu adresáři, což může být užitečné, pokud používáte symbolické odkazy.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `pwd`:

1. Základní použití:
   ```bash
   pwd
   ```

2. Zobrazení fyzické cesty:
   ```bash
   pwd -P
   ```

3. Zobrazení logické cesty (pokud je použito s jinými příkazy):
   ```bash
   cd /some/symlink && pwd -L
   ```

## Tipy
- Používejte `pwd` pravidelně, abyste se ujistili, že se nacházíte v očekávaném adresáři, zejména při práci s více okny terminálu.
- Pokud pracujete s symbolickými odkazy, zvažte použití možnosti `-P`, abyste získali skutečnou fyzickou cestu.
- Příkaz `pwd` je často kombinován s dalšími příkazy pro skriptování, což umožňuje dynamické manipulace se soubory a adresáři.