# [Linux] Bash dstat použití: Monitorování systémových zdrojů v reálném čase

## Přehled
Příkaz `dstat` je nástroj pro monitorování systémových zdrojů v reálném čase. Umožňuje uživatelům sledovat různé aspekty výkonu systému, jako jsou CPU, paměť, diskové operace a síťový provoz, a to vše v jednom přehledném výstupu.

## Použití
Základní syntaxe příkazu `dstat` je následující:

```bash
dstat [možnosti] [argumenty]
```

## Běžné možnosti
- `-c` : Zobrazí využití CPU.
- `-d` : Zobrazí diskové operace.
- `-n` : Zobrazí síťový provoz.
- `-m` : Zobrazí využití paměti.
- `-t` : Zobrazí časové razítko.
- `--help` : Zobrazí nápovědu k příkazu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `dstat`:

1. Základní sledování systému:
   ```bash
   dstat
   ```

2. Sledování CPU a diskových operací:
   ```bash
   dstat -cd
   ```

3. Sledování síťového provozu a paměti:
   ```bash
   dstat -mn
   ```

4. Sledování všech dostupných informací s časovým razítkem:
   ```bash
   dstat -cmdnmt
   ```

5. Uložení výstupu do souboru pro pozdější analýzu:
   ```bash
   dstat -cd --output dstat_output.csv
   ```

## Tipy
- Používejte `dstat` s různými možnostmi pro přizpůsobení výstupu podle vašich potřeb.
- Můžete kombinovat více možností pro získání komplexního přehledu o výkonu systému.
- Uložení výstupu do souboru vám umožní provést analýzu později, což je užitečné pro dlouhodobé sledování.