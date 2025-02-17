# [Linux] Bash head použití: Zobrazí prvních několik řádků souboru

## Přehled
Příkaz `head` v Bashu slouží k zobrazení prvních několika řádků textového souboru. Je užitečný pro rychlé prohlížení obsahu souborů bez nutnosti jejich úplného otevření.

## Použití
Základní syntaxe příkazu `head` je následující:

```bash
head [možnosti] [argumenty]
```

## Běžné možnosti
- `-n [číslo]`: Určuje počet řádků, které se mají zobrazit (výchozí je 10).
- `-q`: Potlačí hlavičky souborů při zobrazení více souborů.
- `-v`: Zobrazí hlavičky souborů i při zobrazení jednoho souboru.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `head`:

1. Zobrazit prvních 10 řádků souboru `soubor.txt`:
   ```bash
   head soubor.txt
   ```

2. Zobrazit prvních 5 řádků souboru `data.csv`:
   ```bash
   head -n 5 data.csv
   ```

3. Zobrazit prvních 20 řádků souboru `log.txt`:
   ```bash
   head -n 20 log.txt
   ```

4. Zobrazit prvních 10 řádků z více souborů `soubor1.txt` a `soubor2.txt`:
   ```bash
   head soubor1.txt soubor2.txt
   ```

5. Zobrazit prvních 10 řádků souboru `config.txt` a zobrazit hlavičku souboru:
   ```bash
   head -v config.txt
   ```

## Tipy
- Používejte `head` v kombinaci s dalšími příkazy, jako je `grep`, pro efektivnější analýzu dat.
- Pokud potřebujete prohlížet velké soubory, `head` je rychlý způsob, jak získat přehled o jejich obsahu.
- Můžete také použít `head` v kombinaci s příkazem `tail` pro analýzu specifických částí souboru.