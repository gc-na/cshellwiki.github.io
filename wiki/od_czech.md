# [Linux] Bash od: Zobrazování souborů v různých formátech

## Overview
Příkaz `od` (octal dump) se používá k zobrazení obsahu souborů v různých formátech, jako jsou oktální, hexadecimální nebo ASCII. Tento nástroj je užitečný pro analýzu binárních souborů a pro debugging.

## Usage
Základní syntaxe příkazu `od` je následující:

```bash
od [options] [arguments]
```

## Common Options
- `-A` : Určuje formát adresy (např. `d` pro desítkový, `o` pro oktální).
- `-t` : Určuje formát výstupu (např. `c` pro znaky, `x` pro hexadecimální).
- `-N` : Určuje počet bajtů k zobrazení.
- `-v` : Zobrazí všechny bajty, včetně opakujících se.

## Common Examples
Zde je několik praktických příkladů použití příkazu `od`:

1. Zobrazení obsahu souboru v hexadecimálním formátu:
   ```bash
   od -t x1 soubor.bin
   ```

2. Zobrazení prvních 16 bajtů souboru v oktálním formátu:
   ```bash
   od -N 16 -A o soubor.bin
   ```

3. Zobrazení obsahu souboru jako znaků:
   ```bash
   od -t c soubor.txt
   ```

4. Zobrazení obsahu souboru v desítkovém formátu:
   ```bash
   od -A d -t u1 soubor.bin
   ```

## Tips
- Používejte volbu `-v`, pokud chcete vidět všechny bajty, což může být užitečné při analýze binárních souborů.
- Kombinujte různé formáty pomocí volby `-t`, abyste získali komplexnější pohled na data.
- Pokud pracujete s velkými soubory, zvažte použití volby `-N`, abyste omezili množství zobrazených dat a usnadnili analýzu.