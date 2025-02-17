# [Linux] Bash lsblk Použití: Zobrazí informace o blokových zařízeních

## Overview
Příkaz `lsblk` slouží k zobrazení informací o blokových zařízeních v systému. Tento příkaz ukazuje strukturu zařízení, jako jsou pevné disky, SSD, USB flash disky a další, a to v hierarchickém formátu.

## Usage
Základní syntaxe příkazu `lsblk` je následující:

```bash
lsblk [options] [arguments]
```

## Common Options
- `-a`, `--all`: Zobrazí všechna bloková zařízení, včetně prázdných.
- `-f`, `--fs`: Zobrazí informace o souborových systémech.
- `-l`, `--list`: Zobrazí zařízení v seznamovém formátu.
- `-o`, `--output`: Umožňuje specifikovat, které sloupce se mají zobrazit.
- `-n`, `--noheadings`: Skryje hlavičky sloupců v výstupu.

## Common Examples
Zde je několik praktických příkladů použití příkazu `lsblk`:

1. Základní zobrazení blokových zařízení:
   ```bash
   lsblk
   ```

2. Zobrazení všech blokových zařízení včetně prázdných:
   ```bash
   lsblk -a
   ```

3. Zobrazení informací o souborových systémech:
   ```bash
   lsblk -f
   ```

4. Zobrazení zařízení v seznamovém formátu:
   ```bash
   lsblk -l
   ```

5. Zobrazení specifických sloupců (např. jméno a velikost):
   ```bash
   lsblk -o NAME,SIZE
   ```

## Tips
- Používejte `lsblk` spolu s dalšími příkazy, jako je `grep`, pro filtrování výstupu.
- Pokud potřebujete podrobnější informace o konkrétním zařízení, zkombinujte `lsblk` s příkazem `blkid`.
- Pro snadnější čitelnost můžete použít volbu `-f` pro zobrazení souborových systémů, což vám pomůže rychleji identifikovat typy zařízení.