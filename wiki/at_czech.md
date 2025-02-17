# [Linux] Bash na at: Plánování úloh

## Přehled
Příkaz `at` slouží k plánování jednorázových úloh, které se mají vykonat v určitém čase. Umožňuje uživatelům naplánovat spouštění skriptů nebo příkazů bez potřeby trvalého běhu skriptu nebo služby.

## Použití
Základní syntaxe příkazu `at` je následující:

```bash
at [možnosti] [argumenty]
```

## Běžné možnosti
- `-f <soubor>`: Určuje soubor, který obsahuje příkazy k vykonání.
- `-m`: Odesílá e-mail po dokončení úlohy, i když nedošlo k žádné chybě.
- `-q <fronta>`: Určuje frontu, do které se úloha zařadí.
- `-l`: Zobrazí seznam naplánovaných úloh.

## Běžné příklady
1. Naplánování příkazu pro spuštění za 1 hodinu:
   ```bash
   echo "echo 'Hello, World!'" | at now + 1 hour
   ```

2. Naplánování skriptu pro spuštění v konkrétní čas:
   ```bash
   at 14:00 < /path/to/script.sh
   ```

3. Použití souboru k naplánování úlohy:
   ```bash
   at -f /path/to/commands.txt now + 2 hours
   ```

4. Zobrazení naplánovaných úloh:
   ```bash
   at -l
   ```

## Tipy
- Ujistěte se, že máte správná oprávnění pro spouštění skriptů, které plánujete.
- Používejte `-m`, pokud chcete být informováni o dokončení úlohy.
- Zkontrolujte, zda je systém správně nastaven na čas a datum, aby úlohy byly vykonány v očekávaném čase.