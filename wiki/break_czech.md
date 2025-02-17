# [Linux] Bash break použití: Ukončení smyčky

## Přehled
Příkaz `break` se používá v Bash skriptech k ukončení smyčky. Když je `break` vykonán, smyčka, ve které se nachází, se okamžitě přeruší a řízení se přesune na příkaz následující po smyčce.

## Použití
Základní syntaxe příkazu `break` je následující:

```bash
break [n]
```

Kde `n` je volitelný argument, který určuje, kolik úrovní smyček má příkaz `break` opustit. Pokud není zadán, `break` opustí pouze nejbližší smyčku.

## Běžné možnosti
- `n`: Určuje počet úrovní smyček, které mají být přerušeny. Pokud je `n` 1, přeruší se pouze nejbližší smyčka. Pokud je `n` 2, přeruší se dvě úrovně smyček atd.

## Běžné příklady

### Příklad 1: Ukončení jedné smyčky
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        break
    fi
    echo $i
done
```
Tento skript vytiskne čísla 1 a 2. Když `i` dosáhne hodnoty 3, smyčka se přeruší.

### Příklad 2: Ukončení vnořené smyčky
```bash
for i in {1..3}; do
    for j in {1..3}; do
        if [ $j -eq 2 ]; then
            break 2
        fi
        echo "i: $i, j: $j"
    done
done
```
Tento skript vytiskne kombinace `i` a `j`, ale když `j` dosáhne hodnoty 2, obě smyčky se přeruší.

### Příklad 3: Použití s while smyčkou
```bash
count=1
while true; do
    echo $count
    if [ $count -eq 5 ]; then
        break
    fi
    ((count++))
done
```
Tento skript vytiskne čísla od 1 do 5 a poté se smyčka přeruší.

## Tipy
- Používejte `break` v kombinaci s podmínkovými příkazy, abyste efektivně řídili tok smyček.
- Pokud potřebujete přerušit více úrovní smyček, nezapomeňte zadat argument `n`.
- Buďte opatrní při používání `break` v komplexních skriptech, abyste se vyhnuli nečekanému ukončení smyček.