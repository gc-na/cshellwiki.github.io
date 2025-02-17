# [Linux] Bash hash použití: Správa uložených cest k příkazům

## Přehled
Příkaz `hash` slouží k správě a zobrazení seznamu uložených cest k příkazům v aktuální shellové relaci. Umožňuje optimalizaci vyhledávání příkazů tím, že ukládá cesty k již provedeným příkazům, což zrychluje jejich opětovné volání.

## Použití
Základní syntaxe příkazu `hash` je následující:

```bash
hash [options] [arguments]
```

## Běžné možnosti
- `-r`: Vymaže všechny uložené cesty a obnoví výchozí nastavení.
- `-l`: Zobrazí seznam všech uložených cest k příkazům.
- `-p <path>`: Přidá specifikovanou cestu k příkazu do seznamu.

## Běžné příklady

### Zobrazení uložených cest
Chcete-li zobrazit všechny aktuálně uložené cesty k příkazům, použijte:

```bash
hash
```

### Vymazání všech uložených cest
Pokud chcete vymazat všechny uložené cesty a obnovit výchozí nastavení, použijte:

```bash
hash -r
```

### Přidání specifické cesty
Pokud chcete přidat konkrétní cestu k příkazu, použijte:

```bash
hash -p /usr/local/bin/mycommand
```

## Tipy
- Používejte `hash -r` po instalaci nového programu, abyste zajistili, že shell bude mít aktuální informace o dostupných příkazech.
- Pravidelně kontrolujte uložené cesty pomocí `hash`, abyste předešli problémům s neexistujícími příkazy.
- Pokud používáte více shellů, mějte na paměti, že `hash` je specifický pro každou relaci.