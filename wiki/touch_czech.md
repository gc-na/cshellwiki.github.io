# [Linux] Bash touch použití: Vytváření nebo aktualizace časových razítek souborů

## Přehled
Příkaz `touch` se v systému Linux používá k vytváření nových souborů nebo k aktualizaci časových razítek existujících souborů. Pokud soubor neexistuje, `touch` ho vytvoří. Pokud existuje, aktualizuje jeho čas posledního přístupu a poslední modifikace na aktuální čas.

## Použití
Základní syntaxe příkazu je následující:

```bash
touch [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Aktualizuje pouze čas posledního přístupu.
- `-m`: Aktualizuje pouze čas poslední modifikace.
- `-c`: Nevytváří nový soubor, pokud neexistuje.
- `-t`: Umožňuje specifikovat časové razítko ve formátu [[CC]YY]MMDD[hhmm[.ss]].

## Běžné příklady
1. **Vytvoření nového souboru:**
   ```bash
   touch novy_soubor.txt
   ```

2. **Aktualizace časového razítka existujícího souboru:**
   ```bash
   touch existujici_soubor.txt
   ```

3. **Aktualizace pouze času posledního přístupu:**
   ```bash
   touch -a existujici_soubor.txt
   ```

4. **Specifikace časového razítka:**
   ```bash
   touch -t 202310251230 novy_soubor.txt
   ```

5. **Nevytvářet soubor, pokud neexistuje:**
   ```bash
   touch -c neexistujici_soubor.txt
   ```

## Tipy
- Používejte `touch` k rychlému vytvoření prázdných souborů pro testování nebo skripty.
- Můžete použít `touch` v kombinaci s jinými příkazy, jako je `find`, pro efektivní správu souborů.
- Pokud potřebujete vytvořit více souborů najednou, jednoduše je vyjmenujte za příkazem `touch`:
  ```bash
  touch soubor1.txt soubor2.txt soubor3.txt
  ```