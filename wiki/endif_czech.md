# [Linux] Bash endif použití: Podmíněné vykonání příkazů

## Overview
Příkaz `endif` se používá v Bash skriptech k označení konce podmíněného bloku, který byl zahájen příkazem `if`. Umožňuje programátorům strukturovat skripty a řídit tok vykonávání na základě podmínek.

## Usage
Základní syntaxe příkazu `endif` je následující:

```bash
endif
```

## Common Options
Příkaz `endif` nemá žádné specifické možnosti, protože se používá pouze jako ukončovací značka pro podmíněné bloky.

## Common Examples

### Příklad 1: Základní použití
Tento příklad ukazuje jednoduchou podmínku, která kontroluje, zda je proměnná `x` větší než 10.

```bash
x=15
if [ $x -gt 10 ]; then
    echo "x je větší než 10"
endif
```

### Příklad 2: Více podmínek
V tomto příkladu se používají dvě podmínky k určení, zda je číslo kladné nebo záporné.

```bash
number=-5
if [ $number -gt 0 ]; then
    echo "Číslo je kladné"
else
    echo "Číslo je záporné"
endif
```

### Příklad 3: Vnořené podmínky
Tento příklad ukazuje, jak používat `endif` v rámci vnořených podmínek.

```bash
value=20
if [ $value -gt 10 ]; then
    echo "Hodnota je větší než 10"
    if [ $value -gt 15 ]; then
        echo "Hodnota je také větší než 15"
    endif
endif
```

## Tips
- Ujistěte se, že každé `if` má odpovídající `endif`, aby se předešlo chybám v syntaxi.
- Používejte odsazení pro zlepšení čitelnosti kódu, zejména při práci s vnořenými podmínkami.
- Testujte skripty v interaktivním režimu, abyste se ujistili, že logika podmínek funguje podle očekávání.