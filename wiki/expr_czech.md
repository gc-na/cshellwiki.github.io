# [Linux] Bash expr použití: Provádí výpočty a manipulaci s řetězci

## Přehled
Příkaz `expr` se používá v Bash pro provádění základních aritmetických operací, porovnávání a manipulaci s řetězci. Umožňuje uživatelům provádět jednoduché výpočty a zpracovávat textové řetězce přímo v příkazovém řádku.

## Použití
Základní syntaxe příkazu `expr` je následující:

```bash
expr [možnosti] [argumenty]
```

## Běžné možnosti
- `+` : Sčítání dvou čísel.
- `-` : Odečítání dvou čísel.
- `*` : Násobení dvou čísel (je třeba použít zpětné lomítko `\` před znakem `*`).
- `/` : Dělení dvou čísel.
- `%` : Zbytek po dělení dvou čísel.
- `=` : Porovnání pro rovnost.
- `!=` : Porovnání pro nerovnost.
- `>` : Porovnání pro větší než.
- `<` : Porovnání pro menší než.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `expr`:

### Aritmetické operace
Sčítání dvou čísel:
```bash
expr 5 + 3
```

Odečítání dvou čísel:
```bash
expr 10 - 4
```

Násobení dvou čísel:
```bash
expr 6 \* 7
```

Dělení dvou čísel:
```bash
expr 20 / 4
```

### Porovnání
Porovnání dvou čísel pro rovnost:
```bash
expr 5 = 5
```

Porovnání dvou čísel pro větší než:
```bash
expr 10 \> 3
```

### Manipulace s řetězci
Získání délky řetězce:
```bash
expr length "Hello, World!"
```

Získání podřetězce:
```bash
expr substr "Hello, World!" 8 5
```

## Tipy
- Při použití operátoru `*` nezapomeňte použít zpětné lomítko `\`, jinak Bash tento znak interpretuje jako zástupný znak.
- `expr` může vracet pouze celočíselné výsledky, takže pro práci s desetinnými čísly je lepší použít jiné nástroje, jako je `bc`.
- Při porovnávání použijte správné operátory pro typ dat, které porovnáváte (např. čísla vs. řetězce).