# [Linux] Bash xz Použití: Komprese a dekomprese souborů

## Přehled
Příkaz `xz` slouží k efektivní kompresi a dekompresi souborů pomocí algoritmu LZMA. Tento nástroj je oblíbený pro svou vysokou kompresní účinnost, což znamená, že dokáže výrazně zmenšit velikost souborů.

## Použití
Základní syntaxe příkazu `xz` je následující:

```bash
xz [možnosti] [argumenty]
```

## Běžné možnosti
- `-d`, `--decompress`: Decompress the specified files.
- `-k`, `--keep`: Keep the original files after compression or decompression.
- `-f`, `--force`: Force compression or decompression, even if the output file already exists.
- `-z`, `--compress`: Compress the specified files (toto je výchozí chování).
- `-9`: Použít maximální úroveň komprese (0-9, kde 9 je nejvyšší).

## Běžné příklady
### Komprese souboru
Pro kompresi souboru `example.txt` použijte:

```bash
xz example.txt
```

### Dekomprese souboru
Pro dekompresi souboru `example.txt.xz` použijte:

```bash
xz -d example.txt.xz
```

### Uložení originálního souboru
Pokud chcete zachovat originální soubor při kompresi, použijte možnost `-k`:

```bash
xz -k example.txt
```

### Komprese s maximální úrovní
Pro kompresi souboru s maximální úrovní komprese:

```bash
xz -9 example.txt
```

## Tipy
- Při práci s velkými soubory zvažte použití možnosti `-k`, abyste neztratili originální data.
- Pokud potřebujete rychlejší kompresi a nepotřebujete maximální úsporu místa, můžete zvolit nižší úroveň komprese (např. `-1`).
- Ujistěte se, že máte dostatek místa na disku, protože komprese může vyžadovat více místa než originální soubor.