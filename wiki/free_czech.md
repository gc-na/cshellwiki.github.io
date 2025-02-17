# [Linux] Bash free příkaz: Zobrazit informace o paměti

## Přehled
Příkaz `free` slouží k zobrazení informací o využití systémové paměti. Umožňuje uživatelům rychle zjistit, kolik paměti je aktuálně využíváno, kolik je volné a kolik je vyrovnávací paměť.

## Použití
Základní syntaxe příkazu je následující:

```bash
free [možnosti]
```

## Běžné možnosti
- `-h`: Zobrazí hodnoty v lidsky čitelném formátu (např. KB, MB).
- `-m`: Zobrazí hodnoty v megabajtech.
- `-g`: Zobrazí hodnoty v gigabajtech.
- `-s [sekundy]`: Aktualizuje výstup každé zadané množství sekund.
- `-t`: Zobrazí celkové využití paměti.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `free`:

1. Základní zobrazení informací o paměti:
   ```bash
   free
   ```

2. Zobrazení informací v lidsky čitelném formátu:
   ```bash
   free -h
   ```

3. Zobrazení informací o paměti v megabajtech:
   ```bash
   free -m
   ```

4. Zobrazení informací o paměti každých 5 sekund:
   ```bash
   free -s 5
   ```

5. Zobrazení celkového využití paměti:
   ```bash
   free -t
   ```

## Tipy
- Používejte možnost `-h`, abyste snadno interpretovali hodnoty paměti.
- Pokud potřebujete sledovat využití paměti v reálném čase, zkombinujte `free` s příkazem `watch`:
  ```bash
  watch free -h
  ```
- Pravidelně kontrolujte využití paměti, zejména na serverech, abyste předešli problémům s výkonem.