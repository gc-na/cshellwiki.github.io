# [Linux] Bash while smyčka: Provádí příkazy opakovaně, dokud je podmínka pravdivá

## Přehled
Příkaz `while` v Bash se používá k opakovanému provádění bloku příkazů, dokud je splněna daná podmínka. To je užitečné pro situace, kdy potřebujete provádět akce, dokud se nezmění určitý stav nebo dokud není splněna určitá podmínka.

## Použití
Základní syntaxe příkazu `while` je následující:

```bash
while [podmínka]; do
    [příkazy]
done
```

## Běžné možnosti
- `-n`: Zkontroluje, zda je řetězec neprázdný.
- `-z`: Zkontroluje, zda je řetězec prázdný.
- `-eq`, `-ne`, `-lt`, `-le`, `-gt`, `-ge`: Porovnávací operátory pro čísla.

## Běžné příklady

### Příklad 1: Základní smyčka
Tento příklad ukazuje, jak provádět příkazy, dokud je proměnná `count` menší než 5.

```bash
count=0
while [ $count -lt 5 ]; do
    echo "Číslo: $count"
    count=$((count + 1))
done
```

### Příklad 2: Čtení ze souboru
Tento příklad čte řádky ze souboru, dokud nedojde ke konci souboru.

```bash
while IFS= read -r line; do
    echo "Řádek: $line"
done < soubor.txt
```

### Příklad 3: Čekání na uživatelský vstup
Tento příklad čeká na uživatelský vstup a provádí akce, dokud uživatel nezadá "exit".

```bash
input=""
while [ "$input" != "exit" ]; do
    read -p "Zadejte něco (nebo 'exit' pro ukončení): " input
    echo "Zadal jste: $input"
done
```

## Tipy
- Ujistěte se, že podmínka ve smyčce se nakonec stane nepravdivou, jinak dojde k nekonečné smyčce.
- Používejte příkaz `break`, pokud chcete smyčku předčasně ukončit.
- Pro lepší čitelnost kódu můžete použít komentáře k vysvětlení složitějších podmínek nebo logiky smyčky.