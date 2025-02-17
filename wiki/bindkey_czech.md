# [Linux] Bash bindkey použití: Správa klávesových zkratek

## Přehled
Příkaz `bindkey` se používá k přiřazení klávesových zkratek v prostředí shellu, zejména v Zsh. Umožňuje uživatelům definovat, jaké akce se mají provádět při stisknutí určitých kláves nebo kombinací kláves.

## Použití
Základní syntaxe příkazu `bindkey` je následující:

```bash
bindkey [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Nastaví režim emacs pro klávesové zkratky.
- `-v`: Nastaví režim vi pro klávesové zkratky.
- `-s`: Přiřadí sekvenci znaků k určité klávese.

## Běžné příklady
Pár praktických příkladů použití příkazu `bindkey`:

1. **Nastavení režimu emacs:**
   ```bash
   bindkey -e
   ```

2. **Nastavení režimu vi:**
   ```bash
   bindkey -v
   ```

3. **Přiřazení klávesové zkratky pro zrušení příkazu:**
   ```bash
   bindkey '^X' 'exit'
   ```

4. **Přiřazení sekvence pro rychlé vyhledávání:**
   ```bash
   bindkey -s '^F' 'find . -name '
   ```

## Tipy
- Přiřazujte klávesové zkratky, které vám usnadní práci a zrychlí vaše úkoly.
- Ujistěte se, že klávesové zkratky, které přiřazujete, nejsou v konfliktu s již existujícími zkratkami.
- Pravidelně kontrolujte a aktualizujte své přiřazení kláves, aby odpovídala vašim aktuálním potřebám a pracovním postupům.