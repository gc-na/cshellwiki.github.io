# [Linux] Bash mpstat použití: Monitorování statistiky CPU

## Přehled
Příkaz `mpstat` slouží k monitorování využití procesoru a zobrazuje statistiky o zatížení CPU v systému. Umožňuje uživatelům sledovat výkon jednotlivých procesorových jader a celkovou zátěž systému.

## Použití
Základní syntaxe příkazu `mpstat` je následující:

```bash
mpstat [možnosti] [argumenty]
```

## Běžné možnosti
- `-P ALL`: Zobrazí statistiky pro všechna procesorová jádra.
- `-u`: Zobrazí využití CPU.
- `-o`: Umožňuje exportovat výstup do souboru.
- `-h`: Zobrazí pomoc a dostupné možnosti.

## Běžné příklady
1. Zobrazení statistik pro všechna jádra CPU:
   ```bash
   mpstat -P ALL
   ```

2. Zobrazení využití CPU v intervalech 5 sekund:
   ```bash
   mpstat 5
   ```

3. Export statistik do souboru:
   ```bash
   mpstat -o CSV 5 > cpu_stats.csv
   ```

4. Zobrazení využití CPU s podrobnostmi:
   ```bash
   mpstat -u
   ```

## Tipy
- Používejte `mpstat` v kombinaci s dalšími nástroji, jako je `top` nebo `htop`, pro komplexnější analýzu výkonu systému.
- Nastavte intervaly, které odpovídají vašim potřebám monitorování, abyste získali přesnější přehled o zatížení CPU.
- Pravidelně zaznamenávejte statistiky do souboru pro pozdější analýzu a sledování trendů výkonu.