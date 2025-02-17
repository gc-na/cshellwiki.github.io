# [Linux] Bash trap použití: Zpracování signálů a ukončení skriptů

## Přehled
Příkaz `trap` v Bash slouží k zachycení a zpracování signálů a událostí, které mohou nastat během běhu skriptu. Umožňuje definovat, co se má stát, když skript obdrží určitý signál, což je užitečné pro správu ukončení skriptu nebo pro provádění úklidových operací.

## Použití
Základní syntaxe příkazu `trap` je následující:

```bash
trap [příkazy] [signály]
```

## Běžné možnosti
- `EXIT`: Spustí příkazy při ukončení skriptu.
- `SIGINT`: Zachytí signál přerušení (Ctrl+C).
- `SIGTERM`: Zachytí signál pro ukončení.
- `ERR`: Spustí příkazy, když dojde k chybě.

## Běžné příklady

### Zachycení signálu SIGINT
Tento příklad ukazuje, jak zachytit signál přerušení a provést úklid před ukončením skriptu.

```bash
#!/bin/bash
trap 'echo "Skript byl přerušen"; exit' SIGINT

while true; do
    echo "Běží skript. Stiskněte Ctrl+C pro přerušení."
    sleep 1
done
```

### Úklid při ukončení skriptu
Tento příklad provede úklidové operace při ukončení skriptu.

```bash
#!/bin/bash
trap 'echo "Provádím úklid..."; rm -f /tmp/tempfile; exit' EXIT

echo "Skript běží. Můžete ho ukončit."
sleep 10
```

### Zachycení chyb
Zde je příklad, jak použít `trap` pro zpracování chyb.

```bash
#!/bin/bash
trap 'echo "Nastala chyba!"' ERR

echo "Tento příkaz selže:"
false
```

## Tipy
- Vždy se ujistěte, že úklidové příkazy v `trap` jsou bezpečné a nezpůsobí další problémy.
- Používejte `trap` pro zajištění, že důležité úkoly (jako odstranění dočasných souborů) budou provedeny, i když skript skončí neočekávaně.
- Můžete kombinovat více signálů a příkazů v jednom příkazu `trap`, což zjednoduší správu různých situací.