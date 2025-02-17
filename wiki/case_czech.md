# [Linux] Bash case použití: Vyhodnocení vzorů

## Přehled
Příkaz `case` v Bash slouží k vyhodnocení proměnné na základě různých vzorů. Umožňuje provádět různé akce v závislosti na hodnotě proměnné, což je užitečné pro podmíněné zpracování.

## Použití
Základní syntaxe příkazu `case` je následující:

```bash
case [proměnná] in
    [vzor1])
        příkaz1 ;;
    [vzor2])
        příkaz2 ;;
    *)
        výchozí_příkaz ;;
esac
```

## Běžné možnosti
Příkaz `case` nemá mnoho specifických možností, ale zde jsou některé důležité aspekty:

- `*` - Zástupný znak, který odpovídá jakékoli hodnotě.
- `;;` - Označuje konec bloku příkazů pro daný vzor.
- `esac` - Ukončuje strukturu `case`.

## Běžné příklady

### Příklad 1: Základní použití
```bash
read -p "Zadejte číslo od 1 do 3: " cislo
case $cislo in
    1)
        echo "Zvolili jste číslo 1." ;;
    2)
        echo "Zvolili jste číslo 2." ;;
    3)
        echo "Zvolili jste číslo 3." ;;
    *)
        echo "Neplatný vstup." ;;
esac
```

### Příklad 2: Použití s textovými hodnotami
```bash
read -p "Zadejte den v týdnu: " den
case $den in
    "pondělí")
        echo "Dnes je pondělí." ;;
    "úterý")
        echo "Dnes je úterý." ;;
    "středa")
        echo "Dnes je středa." ;;
    *)
        echo "Neznámý den." ;;
esac
```

### Příklad 3: Více vzorů
```bash
read -p "Zadejte písmeno (a, b, c): " pismeno
case $pismeno in
    a|A)
        echo "Zvolili jste písmeno A." ;;
    b|B)
        echo "Zvolili jste písmeno B." ;;
    c|C)
        echo "Zvolili jste písmeno C." ;;
    *)
        echo "Neplatný vstup." ;;
esac
```

## Tipy
- Používejte zástupné znaky pro zjednodušení vyhodnocení více hodnot.
- Ujistěte se, že každý blok končí `;;`, aby se předešlo chybám.
- Vždy zahrňte výchozí případ (`*`) pro zpracování neznámých vstupů.