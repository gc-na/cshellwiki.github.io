# [Linux] Bash expand použití: Převod tabulátorů na mezery

## Přehled
Příkaz `expand` slouží k převodu tabulátorů na mezery v textových souborech. Tento příkaz je užitečný pro formátování textu tak, aby byl lépe čitelný a kompatibilní s různými textovými editory, které mohou mít odlišné nastavení pro zobrazení tabulátorů.

## Použití
Základní syntaxe příkazu `expand` je následující:

```
expand [možnosti] [argumenty]
```

## Běžné možnosti
- `-t, --tabs=N` : Nastaví šířku tabulátorů na N mezer (výchozí je 8).
- `-i, --initial` : Převádí pouze tabulátory, které se nacházejí na začátku řádků.
- `-n, --no-tabs` : Nepoužívá tabulátory, místo toho je nahrazuje mezerami.

## Běžné příklady
1. Převod tabulátorů na mezery v souboru `text.txt`:
   ```bash
   expand text.txt
   ```

2. Uložení převedeného výstupu do nového souboru `text_expanded.txt`:
   ```bash
   expand text.txt > text_expanded.txt
   ```

3. Nastavení šířky tabulátorů na 4 mezery:
   ```bash
   expand -t 4 text.txt
   ```

4. Převod tabulátorů pouze na začátku řádků:
   ```bash
   expand -i text.txt
   ```

5. Zobrazení výsledku bez tabulátorů:
   ```bash
   expand -n text.txt
   ```

## Tipy
- Před použitím příkazu `expand` si ověřte, jak jsou tabulátory nastaveny ve vašem textovém editoru, abyste dosáhli požadovaného formátování.
- Můžete kombinovat možnosti pro dosažení specifických výsledků, například `expand -t 4 -i text.txt`.
- Pokud pracujete s velkými soubory, zvažte použití příkazu `less` nebo `more` pro prohlížení výstupu, místo abyste ho ukládali do nového souboru.