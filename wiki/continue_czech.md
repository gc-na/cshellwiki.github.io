# [Linux] Bash continue použití: Pokračuje v cyklu

## Přehled
Příkaz `continue` se používá v Bash skriptech a interaktivních shellech k přeskočení zbývající části aktuální iterace cyklu a pokračování s další iterací. Je to užitečné, když chcete ignorovat určité podmínky a pokračovat v provádění cyklu.

## Použití
Základní syntaxe příkazu `continue` je následující:

```bash
continue [n]
```

Kde `n` je volitelný argument, který určuje, kolik iterací cyklu se má přeskočit.

## Běžné možnosti
- `n`: Volitelný argument, který určuje, kolik iterací cyklu se má přeskočit. Pokud není uvedeno, `continue` přeskočí pouze aktuální iteraci.

## Běžné příklady

### Příklad 1: Základní použití v cyklu for
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        continue
    fi
    echo "Číslo: $i"
done
```
Tento skript vytiskne čísla 1, 2, 4 a 5, protože iterace, kdy je `i` rovno 3, je přeskočena.

### Příklad 2: Použití s podmínkou v cyklu while
```bash
count=0
while [ $count -lt 5 ]; do
    count=$((count + 1))
    if [ $count -eq 2 ]; then
        continue
    fi
    echo "Počítadlo: $count"
done
```
Tento příklad vytiskne hodnoty 1, 3, 4 a 5, protože iterace, kdy je `count` rovno 2, je přeskočena.

### Příklad 3: Přeskočení více iterací
```bash
for i in {1..10}; do
    if [ $i -lt 5 ]; then
        continue 2
    fi
    echo "Číslo: $i"
done
```
Tento skript přeskočí první čtyři iterace a vytiskne čísla 5 až 10.

## Tipy
- Používejte `continue` v cyklech, kde potřebujete ignorovat určité podmínky, abyste udrželi kód přehledný.
- Buďte opatrní při používání argumentu `n`, abyste se vyhnuli nečekaným výsledkům, zejména v komplexních cyklech.
- Testujte skripty s `echo` příkazy před skutečným prováděním, abyste viděli, jak `continue` ovlivňuje tok programu.