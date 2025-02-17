# [Linux] Bash tput použití: Ovládání terminálových vlastností

## Přehled
Příkaz `tput` slouží k ovládání vlastností terminálu, jako je změna barev textu, pozadí nebo pohyb kurzoru. Umožňuje uživatelům přizpůsobit vzhled a chování textového výstupu v terminálu.

## Použití
Základní syntaxe příkazu `tput` je následující:

```bash
tput [možnosti] [argumenty]
```

## Běžné možnosti
- `setaf [číslo]`: Nastaví barvu textu (foreground).
- `setab [číslo]`: Nastaví barvu pozadí (background).
- `clear`: Vymaže obrazovku terminálu.
- `cup [řádek] [sloupec]`: Přesune kurzor na zadanou pozici.
- `bold`: Nastaví text na tučný.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `tput`:

### Změna barvy textu
```bash
tput setaf 1  # Nastaví červenou barvu textu
echo "Toto je červený text."
```

### Změna barvy pozadí
```bash
tput setab 2  # Nastaví zelenou barvu pozadí
echo "Toto je text na zeleném pozadí."
```

### Vymazání obrazovky
```bash
tput clear  # Vymaže terminál
```

### Přesunutí kurzoru
```bash
tput cup 10 20  # Přesune kurzor na řádek 10 a sloupec 20
echo "Toto je text na specifické pozici."
```

### Tučný text
```bash
tput bold  # Nastaví text na tučný
echo "Toto je tučný text."
```

## Tipy
- Používejte `tput` v skriptech pro zlepšení uživatelského rozhraní a vizuální přitažlivosti.
- Experimentujte s různými čísly barev pro dosažení požadovaných efektů; barvy se mohou lišit v závislosti na terminálu.
- Kombinujte více příkazů `tput` pro složitější formátování textu a efektivní prezentaci informací.