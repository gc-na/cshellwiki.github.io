# [Linux] Bash hexdump použití: Zobrazování binárních dat v hexadecimálním formátu

## Přehled
Příkaz `hexdump` slouží k zobrazení obsahu souboru v hexadecimálním formátu. Umožňuje uživatelům analyzovat binární data a zobrazit je v čitelnější podobě, což je užitečné při ladění a analýze souborů.

## Použití
Základní syntaxe příkazu `hexdump` je následující:

```bash
hexdump [možnosti] [argumenty]
```

## Běžné možnosti
- `-C`: Zobrazí výstup v "canonical" formátu, což zahrnuje hexadecimální hodnoty a ASCII reprezentaci.
- `-n <počet>`: Omezí počet bajtů, které se mají zobrazit.
- `-v`: Zobrazí všechny bajty, včetně opakujících se hodnot.
- `-e <formát>`: Umožňuje specifikovat vlastní formát výstupu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `hexdump`:

### Základní hexdump souboru
Zobrazí hexadecimální výstup celého souboru.
```bash
hexdump soubor.bin
```

### Omezit počet bajtů
Zobrazí pouze prvních 16 bajtů souboru.
```bash
hexdump -n 16 soubor.bin
```

### Canonical formát
Zobrazí soubor v kanonickém formátu.
```bash
hexdump -C soubor.bin
```

### Vlastní formát
Zobrazí soubor s vlastním formátem výstupu.
```bash
hexdump -e '1/1 "%02x "' soubor.bin
```

## Tipy
- Používejte možnost `-C`, pokud potřebujete vidět jak hexadecimální hodnoty, tak jejich ASCII reprezentaci, což usnadňuje analýzu.
- Při práci s velkými soubory zvažte použití možnosti `-n`, abyste omezili množství zobrazených dat a usnadnili si orientaci.
- Experimentujte s možností `-e`, abyste vytvořili vlastní formáty výstupu, které mohou lépe vyhovovat vašim potřebám.