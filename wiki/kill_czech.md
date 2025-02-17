# [Linux] Bash kill použití: Ukončení procesů

## Přehled
Příkaz `kill` se používá k ukončení běžících procesů v operačním systému. Umožňuje uživatelům posílat signály procesům, což může zahrnovat žádost o jejich ukončení nebo jinou akci.

## Použití
Základní syntaxe příkazu `kill` je následující:

```
kill [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Zobrazí seznam všech dostupných signálů.
- `-s SIGNAL`: Určuje signál, který má být odeslán (např. `TERM`, `KILL`).
- `-9`: Odesílá signál `SIGKILL`, který okamžitě ukončí proces.

## Běžné příklady
1. Ukončení procesu podle PID:
   ```bash
   kill 1234
   ```
   Tento příkaz odešle výchozí signál `SIGTERM` procesu s PID 1234.

2. Ukončení procesu s použitím signálu `SIGKILL`:
   ```bash
   kill -9 1234
   ```
   Tento příkaz okamžitě ukončí proces s PID 1234 bez ohledu na jeho stav.

3. Odeslání signálu `SIGTERM` na více procesů:
   ```bash
   kill 1234 5678
   ```
   Tento příkaz odešle signál `SIGTERM` procesům s PID 1234 a 5678.

4. Zobrazení dostupných signálů:
   ```bash
   kill -l
   ```
   Tento příkaz zobrazí seznam všech signálů, které můžete použít s příkazem `kill`.

## Tipy
- Před použitím `kill` je dobré zjistit PID procesu pomocí příkazu `ps` nebo `pgrep`.
- Používejte `SIGTERM` před `SIGKILL`, abyste dali procesu šanci na řádné ukončení.
- Pokud se proces neukončuje, zkontrolujte, zda máte potřebná oprávnění k jeho ukončení.