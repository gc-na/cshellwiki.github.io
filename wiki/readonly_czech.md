# [Linux] Bash readonly použití: Nastavení proměnných jako neměnné

## Přehled
Příkaz `readonly` v Bash slouží k nastavení proměnných jako neměnných. Jakmile je proměnná označena jako `readonly`, její hodnota se již nedá změnit. To je užitečné pro ochranu důležitých hodnot v skriptech.

## Použití
Základní syntaxe příkazu je následující:

```bash
readonly [options] [arguments]
```

## Běžné možnosti
- `-p`: Zobrazí všechny aktuální neměnné proměnné.

## Běžné příklady

### Příklad 1: Nastavení proměnné jako neměnné
```bash
my_var="Hello"
readonly my_var
```
Tímto příkazem nastavíte proměnnou `my_var` jako neměnnou. Jakákoliv pokus o změnu její hodnoty vyvolá chybu.

### Příklad 2: Pokus o změnu neměnné proměnné
```bash
my_var="Hello"
readonly my_var
my_var="World"  # Tato řádka vyvolá chybu
```

### Příklad 3: Zobrazení všech neměnných proměnných
```bash
readonly -p
```
Tento příkaz zobrazí seznam všech aktuálně nastavených neměnných proměnných.

## Tipy
- Používejte `readonly` pro ochranu důležitých proměnných, které by neměly být změněny během běhu skriptu.
- Pokud potřebujete změnit hodnotu proměnné, musíte nejprve odstranit její neměnnost pomocí příkazu `unset`.
- Vždy si ověřte, které proměnné jsou nastaveny jako neměnné, abyste se vyhnuli nečekaným chybám.