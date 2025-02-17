# [Linux] Bash history použití: Zobrazení příkazové historie

## Přehled
Příkaz `history` v Bashu slouží k zobrazení seznamu předchozích příkazů, které byly v terminálu zadány. Umožňuje uživatelům snadno přistupovat k dříve použitým příkazům, což může výrazně zjednodušit práci v příkazovém řádku.

## Použití
Základní syntaxe příkazu `history` je následující:

```bash
history [options] [arguments]
```

## Běžné možnosti
- `-c`: Vymaže celou historii příkazů.
- `-d offset`: Odstraní příkaz na daném offsetu z historie.
- `n`: Zobrazí posledních n příkazů.

## Běžné příklady
Zde jsou některé praktické příklady použití příkazu `history`:

1. **Zobrazení celé historie příkazů:**
   ```bash
   history
   ```

2. **Zobrazení posledních 10 příkazů:**
   ```bash
   history 10
   ```

3. **Vymazání historie příkazů:**
   ```bash
   history -c
   ```

4. **Odstranění konkrétního příkazu z historie:**
   ```bash
   history -d 5
   ```

## Tipy
- Používejte klávesu šipka nahoru a dolů pro rychlé procházení předchozími příkazy.
- Můžete použít `!n` pro opětovné spuštění příkazu na pozici n v historii.
- Pravidelně čistěte historii, pokud pracujete s citlivými informacemi, abyste zajistili ochranu soukromí.