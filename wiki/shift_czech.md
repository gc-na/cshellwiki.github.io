# [Linux] Bash shift použití: Posun argumentů v skriptech

## Přehled
Příkaz `shift` v Bash slouží k posunu argumentů skriptu doleva. To znamená, že první argument ($1) se odstraní a všechny ostatní argumenty se posunou o jednu pozici dolů. Tento příkaz je užitečný při zpracovávání argumentů předaných skriptu.

## Použití
Základní syntaxe příkazu `shift` je následující:

```bash
shift [n]
```

Kde `n` je volitelný argument, který určuje, o kolik pozic se mají argumenty posunout. Pokud `n` není uvedeno, výchozí hodnota je 1.

## Běžné možnosti
- `n`: Číslo, které určuje, o kolik pozic se mají argumenty posunout. Například `shift 2` posune argumenty o dvě pozice.

## Běžné příklady

### Příklad 1: Základní použití
Posunout argumenty o jednu pozici:

```bash
#!/bin/bash
echo "Před posunem: $1 $2 $3"
shift
echo "Po posunu: $1 $2 $3"
```

### Příklad 2: Posunout o více pozic
Posunout argumenty o dvě pozice:

```bash
#!/bin/bash
echo "Před posunem: $1 $2 $3 $4"
shift 2
echo "Po posunu: $1 $2 $3 $4"
```

### Příklad 3: Zpracování všech argumentů
Zpracování všech argumentů v cyklu:

```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "Zpracovávám argument: $1"
    shift
done
```

## Tipy
- Používejte `shift` v kombinaci s cykly pro efektivní zpracování argumentů.
- Ujistěte se, že kontrolujete počet argumentů před použitím `shift`, abyste se vyhnuli chybám.
- Pokud potřebujete uchovat původní argumenty, zvažte jejich uložení do pole před posunem.