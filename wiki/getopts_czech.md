# [Linux] Bash getopts Použití: Zpracování argumentů skriptů

## Přehled
Příkaz `getopts` slouží k analýze a zpracování argumentů předávaných skriptům v Bash. Umožňuje snadno definovat a zpracovávat volby a jejich hodnoty, což usnadňuje práci s příkazovými řádky.

## Použití
Základní syntaxe příkazu `getopts` je následující:

```bash
getopts [options] [arguments]
```

## Běžné možnosti
- `-a` : Aktivuje určitou funkci (specifická pro skript).
- `-b` : Nastaví určitou hodnotu (specifická pro skript).
- `-c` : Zobrazí pomocné informace o použití skriptu.

## Běžné příklady
### Příklad 1: Základní použití
Tento příklad ukazuje, jak použít `getopts` k zpracování voleb:

```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Volba A byla zvolena."
      ;;
    b)
      echo "Volba B byla zvolena s hodnotou: $OPTARG"
      ;;
    c)
      echo "Volba C byla zvolena s hodnotou: $OPTARG"
      ;;
    *)
      echo "Neznámá volba."
      ;;
  esac
done
```

### Příklad 2: Zpracování více voleb
Tento skript zpracovává více voleb najednou:

```bash
#!/bin/bash

while getopts "x:y:z:" opt; do
  case $opt in
    x)
      echo "Volba X: $OPTARG"
      ;;
    y)
      echo "Volba Y: $OPTARG"
      ;;
    z)
      echo "Volba Z: $OPTARG"
      ;;
    *)
      echo "Neznámá volba."
      ;;
  esac
done
```

### Příklad 3: Výchozí hodnota pro volbu
Tento příklad ukazuje, jak nastavit výchozí hodnotu pro volbu:

```bash
#!/bin/bash

value="default"

while getopts "v:" opt; do
  case $opt in
    v)
      value=$OPTARG
      ;;
    *)
      echo "Neznámá volba."
      ;;
  esac
done

echo "Hodnota je: $value"
```

## Tipy
- Vždy používejte dvojtečku `:` za volbami, které očekávají argument, aby `getopts` věděl, že potřebuje další hodnotu.
- Používejte `OPTARG` k přístupu k hodnotě argumentu, který byl předán volbě.
- Nezapomeňte na zpracování neznámých voleb, abyste uživatelům poskytli jasnou zpětnou vazbu.