# [Linux] Bash fc použití: Správa historie příkazů

## Přehled
Příkaz `fc` slouží k zobrazení, úpravě a opětovnému spuštění příkazů z historie. Umožňuje uživatelům snadno vyhledávat a modifikovat předchozí příkazy, což zefektivňuje práci v terminálu.

## Použití
Základní syntaxe příkazu `fc` je následující:

```bash
fc [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Zobrazí seznam příkazů z historie.
- `-r`: Zobrazí příkazy v opačném pořadí.
- `-s`: Spustí příkaz bez jeho zobrazení.
- `-n`: Nezobrazí čísla příkazů při výpisu.

## Běžné příklady
1. **Zobrazení posledních 10 příkazů:**
   ```bash
   fc -l -n -10
   ```

2. **Úprava posledního příkazu:**
   ```bash
   fc
   ```
   (Otevře poslední příkaz v editoru pro úpravy.)

3. **Spuštění příkazu s číslem 5 z historie:**
   ```bash
   fc -s 5
   ```

4. **Zobrazení historie příkazů v opačném pořadí:**
   ```bash
   fc -r -l
   ```

## Tipy
- Používejte `fc` k rychlému opravování chyb v předchozích příkazech místo jejich opětovného psaní.
- Nastavte si oblíbený textový editor pro úpravy příkazů pomocí proměnné prostředí `EDITOR`.
- Experimentujte s různými možnostmi `fc`, abyste zjistili, jak mohou zjednodušit vaši práci v terminálu.