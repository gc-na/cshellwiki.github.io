# [Linux] Bash mkfifo použití: Vytváří pojmenované roury

## Přehled
Příkaz `mkfifo` slouží k vytvoření pojmenovaných rour (FIFO - First In, First Out) v systému. Tyto roury umožňují procesům komunikovat mezi sebou, přičemž data jsou přenášena v pořadí, v jakém byla odeslána.

## Použití
Základní syntaxe příkazu je následující:

```
mkfifo [možnosti] [argumenty]
```

## Běžné možnosti
- `-m, --mode=MODE` : Nastaví oprávnění pro nově vytvořenou rouru.
- `--help` : Zobrazí nápovědu k příkazu.
- `--version` : Zobrazí verzi příkazu.

## Běžné příklady
1. Vytvoření základní pojmenované roury:
   ```bash
   mkfifo moje_roura
   ```

2. Vytvoření roury s konkrétními oprávněními:
   ```bash
   mkfifo -m 644 moje_roura
   ```

3. Použití roury v kombinaci s příkazy `echo` a `cat`:
   ```bash
   mkfifo moje_roura
   echo "Ahoj, světe!" > moje_roura &
   cat < moje_roura
   ```

4. Vytvoření více rour najednou:
   ```bash
   mkfifo roura1 roura2 roura3
   ```

## Tipy
- Před použitím roury se ujistěte, že existuje, abyste se vyhnuli chybám.
- Používejte oprávnění roury opatrně, aby nedošlo k nechtěnému přístupu.
- Roury se automaticky odstraní, když se procesy, které je používají, ukončí, což usnadňuje správu zdrojů.