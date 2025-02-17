# [Linux] Bash sed použití: Úprava textových souborů

## Přehled
Příkaz `sed` (stream editor) je mocný nástroj pro zpracování textu v Unixových systémech. Umožňuje provádět různé úpravy textu, jako je nahrazování, mazání nebo vkládání řádků, a to přímo v textových souborech nebo v textových datech, která jsou posílána přes standardní vstup.

## Použití
Základní syntaxe příkazu `sed` je následující:

```bash
sed [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Umožňuje zadat více příkazů `sed`.
- `-i`: Provádí úpravy přímo v souboru (in-place).
- `-n`: Potlačuje výstup, dokud není explicitně vyžádán pomocí příkazu `p`.
- `-f`: Umožňuje načíst příkazy `sed` z externího souboru.

## Běžné příklady

### Nahrazení textu
Nahrazení výskytu slova "stará" slovem "nová" v souboru `soubor.txt`:

```bash
sed 's/stará/nová/g' soubor.txt
```

### Uložení změn přímo do souboru
Provádí nahrazení a ukládá změny přímo do `soubor.txt`:

```bash
sed -i 's/stará/nová/g' soubor.txt
```

### Výběr konkrétních řádků
Zobrazení pouze řádků 2 až 4 ze souboru `soubor.txt`:

```bash
sed -n '2,4p' soubor.txt
```

### Mazání řádků
Odstranění řádků obsahujících slovo "odstranit":

```bash
sed '/odstranit/d' soubor.txt
```

### Vkládání textu
Vložení textu "Nový řádek" před druhý řádek:

```bash
sed '2i Nový řádek' soubor.txt
```

## Tipy
- Vždy si udělejte zálohu souboru před provedením operace s `-i`, abyste předešli ztrátě dat.
- Používejte `-n` spolu s `p` pro zobrazení pouze těch řádků, které vás zajímají, což může být užitečné při práci s velkými soubory.
- Experimentujte s různými příkazy `sed` v testovacím souboru, abyste se seznámili s jeho funkcemi, než je použijete na důležité dokumenty.