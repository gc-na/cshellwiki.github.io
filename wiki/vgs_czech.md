# [Linux] Bash vgs použití: Zobrazí informace o svazcích svazkového managementu

## Přehled
Příkaz `vgs` slouží k zobrazení informací o svazcích spravovaných systémem LVM (Logical Volume Manager). Umožňuje uživatelům rychle získat přehled o dostupných svazcích, jejich velikostech a dalších důležitých parametrech.

## Použití
Základní syntaxe příkazu `vgs` je následující:

```bash
vgs [možnosti] [argumenty]
```

## Běžné možnosti
- `-o, --units`: Umožňuje specifikovat jednotky pro výstup (např. MB, GB).
- `-h, --noheadings`: Skryje hlavičky sloupců ve výstupu.
- `-a, --all`: Zobrazí všechny svazky, včetně neaktivních.
- `--nosuffix`: Zobrazí velikosti bez přípon (např. bez "G" pro gigabyty).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `vgs`:

1. Základní zobrazení informací o svazcích:
   ```bash
   vgs
   ```

2. Zobrazení informací o svazcích s jednotkami v gigabytech:
   ```bash
   vgs -o +pv_size --units g
   ```

3. Zobrazení všech svazků, včetně neaktivních:
   ```bash
   vgs -a
   ```

4. Zobrazení informací bez hlaviček:
   ```bash
   vgs --noheadings
   ```

## Tipy
- Při práci s LVM je dobré pravidelně kontrolovat stav svazků pomocí `vgs`, abyste měli přehled o dostupném prostoru.
- Používejte možnost `--units`, pokud potřebujete výstup v konkrétních jednotkách, což usnadní čtení.
- Zvažte použití skriptů, které automatizují pravidelné kontroly pomocí `vgs`, což vám ušetří čas a úsilí.