# [Linux] Bash time použití: Měření doby běhu příkazů

## Přehled
Příkaz `time` v Bash se používá k měření doby, po kterou se příkaz vykonává. Tento příkaz poskytuje informace o reálném čase, CPU času a systémovém čase, což může být užitečné pro optimalizaci skriptů a analýzu výkonu.

## Použití
Základní syntaxe příkazu `time` je následující:

```bash
time [možnosti] [argumenty]
```

## Běžné možnosti
- `-p`: Zobrazí výstup v jednoduchém formátu, který je snadno čitelný.
- `-o soubor`: Uloží výstup do zadaného souboru místo na standardní výstup.
- `-v`: Zobrazí podrobnější informace o výkonu.

## Běžné příklady
1. Základní použití pro měření doby běhu příkazu `ls`:
   ```bash
   time ls
   ```

2. Uložení výstupu do souboru:
   ```bash
   time -o vysledky.txt ls
   ```

3. Použití s podrobným výstupem:
   ```bash
   time -v sleep 2
   ```

4. Měření doby běhu skriptu:
   ```bash
   time ./moj_skript.sh
   ```

## Tipy
- Používejte možnost `-p`, pokud potřebujete jednoduchý a přehledný výstup.
- Uložení výstupu do souboru může být užitečné pro pozdější analýzu.
- Měření doby běhu různých příkazů vám může pomoci identifikovat úzká místa ve vašich skriptech.