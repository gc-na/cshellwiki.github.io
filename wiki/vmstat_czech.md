# [Linux] Bash vmstat použití: Zobrazení systémových statistik

## Přehled
Příkaz `vmstat` (virtual memory statistics) slouží k zobrazení informací o systému, jako jsou využití paměti, procesy, vstupně-výstupní operace a další statistiky, které pomáhají monitorovat výkon systému.

## Použití
Základní syntaxe příkazu je následující:

```bash
vmstat [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí aktivní a neaktivní paměť.
- `-m`: Zobrazí statistiky o paměťových blocích.
- `-s`: Zobrazí souhrnné statistiky paměti.
- `-t`: Zobrazí časové razítko.
- `delay`: Časový interval mezi jednotlivými výstupy (v sekundách).
- `count`: Počet výstupů, které se mají zobrazit.

## Běžné příklady
1. Zobrazit systémové statistiky každých 5 sekund:

   ```bash
   vmstat 5
   ```

2. Zobrazit aktivní a neaktivní paměť:

   ```bash
   vmstat -a
   ```

3. Zobrazit souhrnné statistiky paměti:

   ```bash
   vmstat -s
   ```

4. Zobrazit statistiky s časovým razítkem každou sekundu po dobu 10 sekund:

   ```bash
   vmstat -t 1 10
   ```

## Tipy
- Používejte `vmstat` v kombinaci s dalšími nástroji, jako je `top` nebo `htop`, pro komplexnější pohled na výkon systému.
- Sledujte dlouhodobé trendy ve využití paměti a procesů, abyste mohli identifikovat potenciální problémy.
- Experimentujte s různými možnostmi a intervaly, abyste našli nejlepší nastavení pro vaše potřeby monitorování.