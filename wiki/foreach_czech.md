# [Linux] Bash foreach použití: Iterace přes seznam

## Přehled
Příkaz `foreach` v Bash slouží k iteraci přes seznam položek a provádění příkazů pro každou položku. Tento příkaz je užitečný při automatizaci úloh, kde je potřeba provést stejnou akci na více souborech nebo hodnotách.

## Použití
Základní syntaxe příkazu `foreach` je následující:

```bash
foreach [položky] [příkazy]
```

## Běžné možnosti
Příkaz `foreach` v Bash nemá specifické možnosti jako jiné příkazy, ale můžete použít standardní příkazy pro manipulaci s proměnnými a cykly.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `foreach`:

### Příklad 1: Iterace přes seznam souborů
```bash
foreach file in *.txt
    echo "Zpracovávám soubor: $file"
end
```

### Příklad 2: Provádění příkazu na každé položce
```bash
foreach item in {1..5}
    echo "Číslo: $item"
end
```

### Příklad 3: Spuštění příkazu pro každý adresář
```bash
foreach dir in /path/to/directories/*
    cd $dir
    echo "Jsem v adresáři: $(pwd)"
end
```

## Tipy
- Ujistěte se, že používáte správnou syntaxi a že příkaz `foreach` je podporován ve vaší verzi shellu.
- Při práci s velkými seznamy položek zvažte použití příkazu `xargs` pro efektivnější zpracování.
- Vždy testujte své skripty na malém vzorku dat, abyste se vyhnuli nechtěným chybám.