# [Linux] Bash col použití: Odstranění formátování textu

## Přehled
Příkaz `col` slouží k odstranění formátování textu, které je generováno například při tisku dokumentů. Tento příkaz je užitečný pro úpravu textových souborů, které obsahují speciální znaky pro formátování, a umožňuje získat čistý text bez těchto znaků.

## Použití
Základní syntaxe příkazu `col` je následující:

```bash
col [možnosti] [argumenty]
```

## Běžné možnosti
- `-b`: Odstraní zpětné znaky (backspaces).
- `-x`: Převede tabulátory na mezery.
- `-f`: Ignoruje formátovací znaky a zpracovává text jako prostý.

## Běžné příklady
1. **Odstranění formátování z textového souboru:**
   ```bash
   col -b < soubor.txt > cisty_soubor.txt
   ```
   Tento příkaz odstraní zpětné znaky ze souboru `soubor.txt` a výstup uloží do `cisty_soubor.txt`.

2. **Převedení tabulátorů na mezery:**
   ```bash
   col -x < soubor.txt > cisty_soubor.txt
   ```
   Tento příkaz nahradí tabulátory mezerami v souboru `soubor.txt`.

3. **Zpracování textu z příkazového výstupu:**
   ```bash
   dmesg | col -b
   ```
   Tento příkaz odstraní formátování z výstupu příkazu `dmesg`, což je užitečné pro zobrazení čistého textu systémových zpráv.

## Tipy
- Při použití příkazu `col` je dobré mít na paměti, že výstup bude vždy formátován jako prostý text, takže se ujistěte, že to odpovídá vašim potřebám.
- Pokud potřebujete kombinovat více možností, můžete je jednoduše přidat do příkazu, například `col -b -x`.
- Pro kontrolu výsledků můžete použít příkaz `cat -A`, který zobrazí všechny znaky, včetně skrytých, což vám pomůže ověřit, zda byl text správně zpracován.