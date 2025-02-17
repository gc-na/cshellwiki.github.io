# [Linux] Bash true použití: Vždy úspěšný příkaz

## Přehled
Příkaz `true` v Bash je jednoduchý příkaz, který vždy vrací úspěšný výstup (exit status 0). Je užitečný v situacích, kdy potřebujete zajistit, aby skript pokračoval bez chyb, nebo jako placeholder pro budoucí příkazy.

## Použití
Základní syntaxe příkazu `true` je následující:

```bash
true [options] [arguments]
```

## Běžné možnosti
Příkaz `true` nemá žádné specifické možnosti, protože jeho jedinou funkcí je vracet úspěšný výstup. 

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `true`:

### 1. Použití v podmínkovém příkazu
```bash
if true; then
    echo "Tento příkaz se vždy vykoná."
fi
```

### 2. Použití v cyklu
```bash
while true; do
    echo "Tento cyklus poběží navždy."
    sleep 1
done
```

### 3. Jako placeholder
```bash
true && echo "Tento příkaz se vykoná, protože true vrací úspěch."
```

## Tipy
- Používejte `true` v skriptech, kde potřebujete zajistit, že se další příkazy vykonají bez ohledu na předchozí chyby.
- Můžete kombinovat `true` s dalšími příkazy pomocí logických operátorů, jako je `&&` a `||`, pro řízení toku skriptu.
- `true` je také užitečné při testování a ladění skriptů, kde potřebujete dočasně vypnout určité části kódu.