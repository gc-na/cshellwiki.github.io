# [Linux] Bash pr: Tiskování textových souborů

## Přehled
Příkaz `pr` slouží k formátování textových souborů pro tisk. Umožňuje rozdělit text na sloupce, přidat záhlaví a zápatí, a také upravit okraje, což usnadňuje čtení a tisk dokumentů.

## Použití
Základní syntaxe příkazu je následující:

```bash
pr [možnosti] [argumenty]
```

## Běžné možnosti
- `-h, --header` : Přidá záhlaví na každou stránku.
- `-t, --omit-header` : Skryje záhlaví a zápatí.
- `-s, --spaces` : Určuje počet mezer mezi sloupci.
- `-l, --length` : Nastaví délku stránky v řádcích.
- `-w, --width` : Nastaví šířku stránky v znacích.

## Běžné příklady
1. **Základní formátování souboru:**
   ```bash
   pr soubor.txt
   ```

2. **Formátování souboru s přidáním záhlaví:**
   ```bash
   pr -h "Moje Záhlaví" soubor.txt
   ```

3. **Tisk souboru bez záhlaví a zápatí:**
   ```bash
   pr -t soubor.txt
   ```

4. **Rozdělení textu do dvou sloupců:**
   ```bash
   pr -s 2 soubor.txt
   ```

5. **Nastavení délky stránky na 50 řádků:**
   ```bash
   pr -l 50 soubor.txt
   ```

## Tipy
- Při tisku delších dokumentů zvažte použití možnosti `-l` pro lepší kontrolu nad stránkováním.
- Pokud potřebujete dokument vytisknout na více sloupcích, experimentujte s různými hodnotami pro `-s`.
- Ujistěte se, že váš textový soubor má správné formátování, aby se výsledný tisk snadno četl.