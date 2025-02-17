# [Linux] Bash nice použití: Řízení priority procesů

## Přehled
Příkaz `nice` slouží k nastavení priority procesů v systému Linux. Umožňuje uživatelům spouštět procesy s nižší nebo vyšší prioritou, což ovlivňuje, jak moc CPU času dostanou ve srovnání s jinými procesy.

## Použití
Základní syntaxe příkazu je následující:

```bash
nice [možnosti] [argumenty]
```

## Běžné možnosti
- `-n, --adjustment=N`: Nastaví hodnotu priority procesu. Může být kladná (nižší priorita) nebo záporná (vyšší priorita).
- `-h, --help`: Zobrazí nápovědu k příkazu.
- `--version`: Zobrazí verzi příkazu.

## Běžné příklady
1. Spuštění procesu s výchozí prioritou:
   ```bash
   nice myscript.sh
   ```

2. Spuštění procesu s nižší prioritou (např. +10):
   ```bash
   nice -n 10 myscript.sh
   ```

3. Spuštění procesu s vyšší prioritou (např. -5):
   ```bash
   nice -n -5 myscript.sh
   ```

4. Zobrazení aktuálního nastavení priority pro běžící proces:
   ```bash
   ps -o pid,ni,cmd
   ```

## Tipy
- Používejte `nice` pro procesy, které nejsou časově kritické, abyste uvolnili systémové prostředky pro důležitější úkoly.
- Pokud potřebujete změnit prioritu již běžícího procesu, můžete použít příkaz `renice`.
- Při nastavování záporné priority je třeba mít administrátorská práva (root).