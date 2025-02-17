# [Linux] Bash tail použití: Zobrazí poslední řádky souboru

## Přehled
Příkaz `tail` se používá k zobrazení posledních několika řádků textového souboru. Je užitečný pro sledování logů nebo pro rychlé prohlížení obsahu souboru, aniž byste museli otevírat celý soubor.

## Použití
Základní syntaxe příkazu `tail` je následující:

```
tail [možnosti] [argumenty]
```

## Běžné možnosti
- `-n [číslo]`: Určuje počet řádků, které se mají zobrazit. Například `-n 10` zobrazí posledních 10 řádků.
- `-f`: Sledování souboru v reálném čase. Nové řádky přidané do souboru se automaticky zobrazí.
- `-c [číslo]`: Zobrazí posledních [číslo] bajtů souboru místo řádků.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `tail`:

1. Zobrazit posledních 10 řádků souboru:
   ```bash
   tail soubor.txt
   ```

2. Zobrazit posledních 20 řádků souboru:
   ```bash
   tail -n 20 soubor.txt
   ```

3. Sledovat log soubor v reálném čase:
   ```bash
   tail -f /var/log/syslog
   ```

4. Zobrazit posledních 100 bajtů souboru:
   ```bash
   tail -c 100 soubor.txt
   ```

## Tipy
- Používejte `tail -f` pro monitorování logů, abyste mohli okamžitě vidět nové záznamy.
- Kombinujte `tail` s dalšími příkazy, jako je `grep`, pro filtrování specifických řádků. Například:
  ```bash
  tail -f soubor.log | grep "chyba"
  ```
- Pokud potřebujete zobrazit více než posledních 10 řádků, můžete použít `-n` s libovolným číslem, které potřebujete.