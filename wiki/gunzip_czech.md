# [Linux] Bash gunzip použití: Rozbalení souborů gzip

## Přehled
Příkaz `gunzip` slouží k rozbalení souborů, které byly komprimovány pomocí formátu gzip. Tento příkaz je užitečný pro dekompresi souborů a obnovení jejich původní velikosti a obsahu.

## Použití
Základní syntaxe příkazu je následující:

```bash
gunzip [možnosti] [argumenty]
```

## Běžné možnosti
- `-c`: Výstup rozbaleného obsahu na standardní výstup místo do souboru.
- `-f`: Přepsat existující soubory bez dotazu.
- `-k`: Zachovat původní soubor při rozbalování.
- `-v`: Zobrazit podrobnosti o rozbalování, včetně velikosti souboru před a po dekompresi.

## Běžné příklady
Rozbalení souboru `example.gz`:

```bash
gunzip example.gz
```

Rozbalení souboru a zachování původního souboru:

```bash
gunzip -k example.gz
```

Zobrazení rozbaleného obsahu na standardním výstupu:

```bash
gunzip -c example.gz
```

Rozbalení více souborů najednou:

```bash
gunzip file1.gz file2.gz file3.gz
```

## Tipy
- Před rozbalením souboru se ujistěte, že máte dostatek místa na disku pro obnovení původního souboru.
- Používejte možnost `-v`, pokud chcete sledovat proces dekomprese a zkontrolovat velikosti souborů.
- Pokud často pracujete s gzip soubory, zvažte použití aliasu pro zjednodušení příkazů.