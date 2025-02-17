# [Linux] Bash iostat použití: Monitorování vstupně-výstupních statistik

## Přehled
Příkaz `iostat` slouží k monitorování vstupně-výstupních statistik systému, což zahrnuje informace o využití procesoru a vstupně-výstupních operacích na zařízeních. Pomocí tohoto příkazu můžete sledovat výkon disků a identifikovat potenciální problémy s výkonem.

## Použití
Základní syntaxe příkazu `iostat` je následující:

```bash
iostat [možnosti] [argumenty]
```

## Běžné možnosti
- `-c`: Zobrazí pouze statistiky procesoru.
- `-d`: Zobrazí pouze statistiky pro zařízení.
- `-x`: Zobrazí rozšířené statistiky pro zařízení.
- `-t`: Zobrazí časové razítko pro každou sadu statistik.
- `interval`: Časový interval (v sekundách) mezi jednotlivými výstupy.

## Běžné příklady
1. Základní použití pro zobrazení statistik:
   ```bash
   iostat
   ```

2. Zobrazení pouze statistik procesoru:
   ```bash
   iostat -c
   ```

3. Zobrazení statistik pro zařízení s rozšířenými informacemi:
   ```bash
   iostat -xd 1
   ```

4. Zobrazení statistik s časovým razítkem:
   ```bash
   iostat -t 2
   ```

5. Zobrazení statistik každé 5 sekund:
   ```bash
   iostat 5
   ```

## Tipy
- Používejte možnost `-x` pro podrobnější analýzu výkonu disků, což vám pomůže lépe porozumět, jak zařízení reagují na zátěž.
- Kombinujte `iostat` s dalšími nástroji, jako je `vmstat` nebo `mpstat`, pro komplexnější pohled na výkon systému.
- Sledujte dlouhodobé trendy ve statistikách, abyste mohli identifikovat potenciální problémy s výkonem dříve, než se stanou kritickými.