# [Linux] Bash iconv použití: Převod textových kódování

## Přehled
Příkaz `iconv` slouží k převodu textových souborů mezi různými kódováními znaků. Je užitečný pro zajištění kompatibility textových dat, která mohou být uložena v různých formátech.

## Použití
Základní syntaxe příkazu `iconv` je následující:

```bash
iconv [možnosti] [argumenty]
```

## Běžné možnosti
- `-f, --from-code=KÓDOVÁNÍ` – Určuje kódování vstupního textu.
- `-t, --to-code=KÓDOVÁNÍ` – Určuje kódování výstupního textu.
- `-o, --output=SOUBOR` – Umožňuje specifikovat výstupní soubor.
- `-l, --list` – Zobrazí seznam všech podporovaných kódování.

## Běžné příklady
Převod souboru z UTF-8 na ISO-8859-1:

```bash
iconv -f UTF-8 -t ISO-8859-1 soubor.txt -o soubor_iso.txt
```

Převod souboru z Windows-1250 na UTF-8:

```bash
iconv -f WINDOWS-1250 -t UTF-8 soubor_windows.txt -o soubor_utf8.txt
```

Zobrazení seznamu podporovaných kódování:

```bash
iconv -l
```

## Tipy
- Před převodem si vždy ověřte, jaké kódování má váš vstupní soubor, abyste předešli chybám.
- Pokud pracujete s velkými soubory, můžete použít příkaz `iconv` v kombinaci s dalšími příkazy, jako je `grep` nebo `awk`, pro efektivnější zpracování dat.
- Uložte si často používané příkazy do skriptu, abyste je mohli snadno znovu použít.