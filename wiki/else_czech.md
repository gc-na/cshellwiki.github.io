# [Linux] Bash else použití: Podmínková logika v skriptech

## Přehled
Příkaz `else` v Bash slouží k implementaci podmínkové logiky v skriptech. Umožňuje provádět různé akce na základě splnění nebo nesplnění určité podmínky.

## Použití
Základní syntaxe příkazu `else` je následující:

```bash
if [ podmínka ]; then
    # příkazy, pokud je podmínka pravdivá
else
    # příkazy, pokud je podmínka nepravdivá
fi
```

## Běžné možnosti
Příkaz `else` nemá žádné specifické možnosti, ale je často používán v kombinaci s příkazem `if`, který umožňuje definovat podmínky.

## Běžné příklady

### Příklad 1: Základní použití
Tento příklad ukazuje, jak použít `else` k provedení různých příkazů na základě podmínky.

```bash
#!/bin/bash
if [ -f "soubor.txt" ]; then
    echo "Soubor existuje."
else
    echo "Soubor neexistuje."
fi
```

### Příklad 2: Kontrola proměnné
V tomto příkladu se kontroluje hodnota proměnné a podle toho se vykonají různé akce.

```bash
#!/bin/bash
jmeno="Alice"
if [ "$jmeno" == "Bob" ]; then
    echo "Ahoj, Bob!"
else
    echo "Ahoj, $jmeno!"
fi
```

### Příklad 3: Více podmínek
Můžete také kombinovat `if`, `else` a `elif` pro složitější logiku.

```bash
#!/bin/bash
cislo=10
if [ $cislo -gt 10 ]; then
    echo "Číslo je větší než 10."
elif [ $cislo -eq 10 ]; then
    echo "Číslo je rovno 10."
else
    echo "Číslo je menší než 10."
fi
```

## Tipy
- Vždy uzavírejte bloky `if` pomocí `fi`, aby byl skript správně strukturován.
- Používejte odsazení pro lepší čitelnost kódu.
- Testujte podmínky s různými typy dat (např. čísla, řetězce) a ujistěte se, že používáte správné operátory pro porovnání.