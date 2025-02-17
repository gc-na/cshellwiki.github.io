# [Linux] Bash set použití: Nastavení shellových vlastností

## Přehled
Příkaz `set` v Bash slouží k nastavení nebo zobrazení různých vlastností shellu a proměnných prostředí. Umožňuje uživatelům konfigurovat chování shellu podle svých potřeb.

## Použití
Základní syntaxe příkazu `set` je následující:

```
set [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Ukončí skript při jakékoliv chybě.
- `-u`: Oznámí chybu, pokud se pokusíte použít neexistující proměnnou.
- `-x`: Zobrazí příkazy a jejich argumenty při vykonávání, což je užitečné pro ladění.
- `+e`: Zruší chování ukončení skriptu při chybách (opposite of `-e`).
- `+u`: Zruší upozornění na neexistující proměnné (opposite of `-u`).

## Běžné příklady
1. **Nastavení ukončení skriptu při chybě:**
   ```bash
   set -e
   ```
   Tento příkaz zajistí, že skript se okamžitě ukončí, pokud dojde k chybě.

2. **Zobrazení příkazů při vykonávání:**
   ```bash
   set -x
   ```
   Tento příkaz aktivuje režim ladění, kde se zobrazují všechny vykonávané příkazy.

3. **Zastavení upozornění na neexistující proměnné:**
   ```bash
   set +u
   ```
   Tímto příkazem se zruší upozornění na pokusy o použití neexistujících proměnných.

4. **Kombinace možností:**
   ```bash
   set -e -u -x
   ```
   Tento příkaz nastaví všechny tři možnosti najednou, což je užitečné pro robustní skripty.

## Tipy
- Používejte `set -e` pro zajištění, že váš skript nebude pokračovat v případě chyby, což může zabránit nechtěným následkům.
- Aktivujte `set -x` při ladění skriptů, abyste viděli, co se děje v reálném čase.
- Zvažte použití `set +u` pouze v případě, že víte, že některé proměnné nemusí být nastaveny, abyste se vyhnuli zbytečným chybám.