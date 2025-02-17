# [Linux] Bash env použití: Správa prostředí

## Přehled
Příkaz `env` se používá k zobrazení nebo nastavení prostředí pro spuštění příkazů v Bash. Umožňuje uživatelům spouštět programy s upravenými proměnnými prostředí, což může být užitečné při testování nebo při potřebě specifických konfigurací.

## Použití
Základní syntaxe příkazu `env` je následující:

```bash
env [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Spustí příkaz s prázdným prostředím.
- `-u VAR`: Odstraní proměnnou prostředí `VAR` před spuštěním příkazu.
- `VAR=value`: Nastaví proměnnou prostředí `VAR` na `value` před spuštěním příkazu.

## Běžné příklady

1. **Zobrazení aktuálních proměnných prostředí:**
   ```bash
   env
   ```

2. **Spuštění příkazu s prázdným prostředím:**
   ```bash
   env -i bash
   ```

3. **Nastavení proměnné prostředí a spuštění příkazu:**
   ```bash
   env MY_VAR=Hello world
   ```

4. **Odstranění proměnné prostředí před spuštěním příkazu:**
   ```bash
   env -u MY_VAR echo "MY_VAR is unset"
   ```

## Tipy
- Používejte `env` k testování, jak se programy chovají s různými proměnnými prostředí.
- Pokud potřebujete spustit skript s konkrétními proměnnými, můžete použít `env` k jejich dočasnému nastavení.
- Při používání `-i` buďte opatrní, protože to odstraní všechny proměnné prostředí, což může ovlivnit chování příkazů.