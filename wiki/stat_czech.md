# [Linux] Bash stat použití: Získání informací o souborech

## Přehled
Příkaz `stat` se používá k zobrazení podrobných informací o souborech a adresářích v systému. Umožňuje uživatelům získat informace jako velikost souboru, čas poslední modifikace, oprávnění a další metadata.

## Použití
Základní syntaxe příkazu `stat` je následující:

```bash
stat [možnosti] [argumenty]
```

## Běžné možnosti
- `-c` : Umožňuje specifikovat formát výstupu pomocí formátovacích specifikátorů.
- `--format` : Alternativa k `-c`, umožňuje definovat vlastní formát výstupu.
- `-f` : Zobrazí informace o systému souborů, ve kterém se soubor nachází.
- `--help` : Zobrazí nápovědu k příkazu `stat`.
- `--version` : Zobrazí verzi příkazu `stat`.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `stat`:

1. Získání základních informací o souboru:
   ```bash
   stat soubor.txt
   ```

2. Zobrazení informací o adresáři:
   ```bash
   stat /cesta/k/adresáři
   ```

3. Použití formátování pro zobrazení pouze velikosti a času poslední modifikace:
   ```bash
   stat -c "Velikost: %s, Poslední modifikace: %y" soubor.txt
   ```

4. Získání informací o systému souborů:
   ```bash
   stat -f /cesta/k/souboru
   ```

## Tipy
- Používejte formátovací možnosti pro přizpůsobení výstupu podle svých potřeb.
- Pokud potřebujete rychle zjistit informace o více souborech, můžete je uvést jako argumenty za příkaz `stat`.
- Nezapomeňte, že příkaz `stat` může být užitečný při skriptování pro automatizaci úloh souvisejících se soubory.