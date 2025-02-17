# [Linux] Bash lvcreate Použití: Vytváření logických svazků

## Přehled
Příkaz `lvcreate` se používá k vytváření nových logických svazků v rámci systému správy svazků LVM (Logical Volume Manager). Tento nástroj umožňuje efektivní správu diskového prostoru a usnadňuje rozšiřování nebo zmenšování svazků podle potřeby.

## Použití
Základní syntaxe příkazu je následující:

```bash
lvcreate [možnosti] [argumenty]
```

## Běžné možnosti
- `-n, --name <název>`: Určuje název nového logického svazku.
- `-L, --size <velikost>`: Definuje velikost logického svazku.
- `-l, --extents <rozsah>`: Umožňuje specifikovat velikost v extentech.
- `-m, --mirrors <počet>`: Určuje počet zrcadlených svazků.
- `-Z, --zero nahrát`: Určuje, zda se má logický svazek při vytváření inicializovat nulovými hodnotami.

## Běžné příklady
1. Vytvoření logického svazku s názvem `data` o velikosti 10 GB:
   ```bash
   lvcreate -n data -L 10G vg1
   ```

2. Vytvoření logického svazku s názvem `backup` o velikosti 5 GB a inicializace nulovými hodnotami:
   ```bash
   lvcreate -n backup -L 5G -Z y vg1
   ```

3. Vytvoření zrcadleného logického svazku s názvem `mirror_data`:
   ```bash
   lvcreate -n mirror_data -m 1 -L 20G vg1
   ```

4. Vytvoření logického svazku s velikostí určenou v extentech (např. 100 extents):
   ```bash
   lvcreate -n extent_volume -l 100 vg1
   ```

## Tipy
- Před použitím `lvcreate` se ujistěte, že máte vytvořený fyzický svazek a skupinu svazků.
- Používejte smysluplné názvy pro logické svazky, aby bylo snadné je později identifikovat.
- Pravidelně kontrolujte stav svazků pomocí příkazu `lvdisplay`, abyste měli přehled o využití diskového prostoru.