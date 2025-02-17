# [Linux] Bash source použití: Spuštění skriptů v aktuálním shellu

## Přehled
Příkaz `source` se používá k načtení a spuštění obsahu skriptu v aktuálním shellovém prostředí. To znamená, že jakékoli proměnné nebo funkce definované ve skriptu budou k dispozici i po jeho dokončení, což je užitečné pro konfiguraci prostředí nebo načítání funkcí.

## Použití
Základní syntaxe příkazu `source` je následující:

```bash
source [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`, `--help`: Zobrazí nápovědu k příkazu.
- `-v`, `--verbose`: Zobrazí příkazy, které se vykonávají.

## Běžné příklady

### Načtení skriptu
Načtení skriptu `myscript.sh` do aktuálního shellu:

```bash
source myscript.sh
```

### Použití s proměnnými
Pokud skript obsahuje proměnné, můžete je použít po jeho načtení:

```bash
# myscript.sh
export MY_VAR="Hello, World!"

# V shellu
source myscript.sh
echo $MY_VAR  # Výstup: Hello, World!
```

### Načtení skriptu s argumenty
Pokud potřebujete předat argumenty, můžete použít příkaz `.` (tečka), který je synonymem pro `source`:

```bash
# myscript.sh
echo "Argument: $1"

# V shellu
. myscript.sh "Test argument"  # Výstup: Argument: Test argument
```

## Tipy
- Používejte `source` pro skripty, které mění prostředí, jako jsou skripty pro nastavení proměnných prostředí.
- Pokud skript nefunguje, zkontrolujte, zda je správně napsaný a zda má potřebná oprávnění.
- Pro rychlé testování skriptů můžete použít `source`, abyste se vyhnuli vytváření nového shellu.