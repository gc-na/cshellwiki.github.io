# [Linux] Bash clear použití: Vyčistit terminál

## Přehled
Příkaz `clear` slouží k vyčištění obsahu terminálu. Po jeho spuštění se obrazovka terminálu vyčistí, což může být užitečné pro zlepšení přehlednosti a organizace při práci s příkazovým řádkem.

## Použití
Základní syntaxe příkazu je následující:

```bash
clear [možnosti] [argumenty]
```

## Běžné možnosti
- `-x` : Vyčistí terminál a zároveň vymaže historii příkazů, což znamená, že se již nebudou zobrazovat předchozí příkazy.

## Běžné příklady
1. **Základní vyčištění terminálu**:
   ```bash
   clear
   ```

2. **Vyčištění terminálu s vymazáním historie příkazů**:
   ```bash
   clear -x
   ```

3. **Použití v skriptu**:
   Pokud chcete vyčistit terminál v rámci skriptu, můžete použít příkaz `clear` na začátku skriptu:
   ```bash
   #!/bin/bash
   clear
   echo "Toto je nový skript."
   ```

## Tipy
- Používejte `clear` pravidelně, abyste udrželi svůj terminál přehledný, zejména při práci s dlouhými výstupy.
- Můžete kombinovat `clear` s dalšími příkazy v skriptech pro automatizaci úloh a zlepšení uživatelského rozhraní.
- Pokud používáte terminál s více okny, nezapomeňte, že `clear` vyčistí pouze aktivní okno.