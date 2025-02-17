# [Linux] Bash iotop použití: Monitorování I/O aktivit procesů

## Přehled
Příkaz `iotop` slouží k monitorování vstupně-výstupních (I/O) aktivit procesů v reálném čase. Umožňuje uživatelům sledovat, které procesy využívají diskové operace, což je užitečné pro diagnostiku výkonu systému.

## Použití
Základní syntaxe příkazu `iotop` je následující:

```bash
iotop [možnosti] [argumenty]
```

## Běžné možnosti
- `-o`, `--only`: Zobrazí pouze procesy, které aktuálně vykonávají I/O operace.
- `-b`, `--batch`: Spustí `iotop` v dávkovém režimu, což je užitečné pro logování.
- `-n NUM`, `--iter NUM`: Určuje počet iterací, které se mají provést v dávkovém režimu.
- `-d SEC`, `--delay SEC`: Nastavuje zpoždění mezi aktualizacemi v sekundách.

## Běžné příklady
1. Základní spuštění `iotop` pro sledování I/O aktivit:
   ```bash
   iotop
   ```

2. Zobrazení pouze procesů s aktivními I/O operacemi:
   ```bash
   iotop -o
   ```

3. Spuštění `iotop` v dávkovém režimu s 5 sekundovým zpožděním:
   ```bash
   iotop -b -d 5
   ```

4. Záznam I/O aktivit po dobu 10 iterací:
   ```bash
   iotop -b -n 10
   ```

## Tipy
- Používejte `iotop` s oprávněními superuživatele (např. pomocí `sudo`), abyste viděli všechny procesy, včetně těch, které patří jiným uživatelům.
- V dávkovém režimu můžete výstup přesměrovat do souboru pro pozdější analýzu, například:
  ```bash
  iotop -b -n 10 > iotop_log.txt
  ```
- Sledujte procesy, které mají vysokou hodnotu I/O, abyste identifikovali potenciální problémy s výkonem.