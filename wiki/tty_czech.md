# [Linux] Bash tty použití: Zobrazí název terminálu

## Přehled
Příkaz `tty` slouží k zobrazení názvu terminálu, na kterém je příkaz spuštěn. Tento název může být užitečný pro skripty a diagnostiku, kdy potřebujete zjistit, na jakém terminálu pracujete.

## Použití
Základní syntaxe příkazu `tty` je následující:

```bash
tty [možnosti]
```

## Běžné možnosti
- `-s`: Tato možnost způsobí, že příkaz nebude nic vypisovat na standardní výstup, pouze vrátí stavový kód (0, pokud je terminál připojen, jinak 1).

## Běžné příklady
1. Základní použití příkazu `tty` pro zobrazení názvu aktuálního terminálu:
    ```bash
    tty
    ```

2. Použití s možností `-s` pro kontrolu, zda je terminál připojen:
    ```bash
    tty -s && echo "Terminál je připojen" || echo "Terminál není připojen"
    ```

3. Zapsání názvu terminálu do proměnné:
    ```bash
    TERMINAL_NAME=$(tty)
    echo "Název terminálu je: $TERMINAL_NAME"
    ```

## Tipy
- Používejte `tty` v skriptech, abyste zjistili, na jakém terminálu skript běží, což může pomoci při ladění.
- Pokud potřebujete zjistit, zda je terminál připojen, použijte možnost `-s` pro efektivní kontrolu bez zbytečného výstupu.