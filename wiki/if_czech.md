# [Linux] Bash if příkaz: Podmíněné vyhodnocení

## Přehled
Příkaz `if` v Bash slouží k provádění podmíněného vyhodnocení. Umožňuje spouštět příkazy na základě splnění určitých podmínek. To je užitečné pro řízení toku skriptů a rozhodování na základě výsledků testů.

## Použití
Základní syntaxe příkazu `if` je následující:

```bash
if [ podmínka ]; then
    příkaz1
    příkaz2
fi
```

## Běžné možnosti
- `-e`: Zkontroluje, zda soubor existuje.
- `-d`: Zkontroluje, zda je cesta k adresáři.
- `-f`: Zkontroluje, zda je cesta k souboru.
- `-z`: Zkontroluje, zda je řetězec prázdný.
- `-n`: Zkontroluje, zda je řetězec neprázdný.

## Běžné příklady

### Příklad 1: Kontrola existence souboru
```bash
if [ -e "soubor.txt" ]; then
    echo "Soubor existuje."
else
    echo "Soubor neexistuje."
fi
```

### Příklad 2: Kontrola prázdného řetězce
```bash
jmeno=""
if [ -z "$jmeno" ]; then
    echo "Jméno je prázdné."
else
    echo "Jméno není prázdné."
fi
```

### Příklad 3: Kontrola adresáře
```bash
if [ -d "/cesta/k/adresari" ]; then
    echo "Adresář existuje."
else
    echo "Adresář neexistuje."
fi
```

## Tipy
- Vždy uzavírejte podmínky do hranatých závorek `[ ]` a nezapomeňte na mezery kolem podmínky.
- Používejte `elif` pro více podmínek, abyste se vyhnuli zanořeným `if` blokům.
- Pro složitější podmínky můžete použít logické operátory `&&` (a) a `||` (nebo) pro kombinaci více podmínek.