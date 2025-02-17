# [Linux] Bash bg použití: Pozastavení úloh na pozadí

## Přehled
Příkaz `bg` se používá v Bash pro obnovení pozastavených úloh a jejich spuštění na pozadí. To umožňuje uživatelům pokračovat v práci v terminálu, zatímco úloha běží na pozadí.

## Použití
Základní syntaxe příkazu `bg` je následující:

```bash
bg [možnosti] [argumenty]
```

## Běžné možnosti
- `job_spec`: Specifikuje úlohu, kterou chcete spustit na pozadí. Může to být číslo úlohy nebo název úlohy.
- `-n`: Spustí úlohu na pozadí, ale neprovádí žádnou akci, pokud je úloha již na pozadí.

## Běžné příklady
1. **Obnovení poslední pozastavené úlohy na pozadí:**
   ```bash
   bg
   ```

2. **Obnovení konkrétní úlohy na pozadí podle čísla úlohy:**
   ```bash
   bg %1
   ```

3. **Obnovení úlohy s názvem:**
   ```bash
   bg my_task
   ```

4. **Obnovení úlohy na pozadí s přesměrováním výstupu:**
   ```bash
   bg %2 > output.txt &
   ```

## Tipy
- Používejte příkaz `jobs` pro zobrazení seznamu aktuálních úloh a jejich stavů.
- Pokud potřebujete úlohu zastavit, můžete použít příkaz `fg` pro její obnovení na popředí.
- Pamatujte, že úlohy běžící na pozadí mohou stále generovat výstup, takže je dobré je přesměrovat do souboru, pokud nechcete, aby zaplnily terminál.