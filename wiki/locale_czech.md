# [Linux] Bash locale použití: Zobrazení informací o lokalizaci

## Přehled
Příkaz `locale` slouží k zobrazení informací o aktuálním nastavení lokalizace v systému. Tyto informace zahrnují jazyk, formát data a času, měnu a další regionální nastavení, která ovlivňují chování programů a aplikací.

## Použití
Základní syntaxe příkazu `locale` je následující:

```bash
locale [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechny dostupné lokalizace.
- `-m`: Zobrazí seznam dostupných mapování znaků.
- `-k`: Zobrazí konkrétní informace o lokalizaci.
- `-c`: Zobrazí pouze informace o aktuální lokalizaci.

## Běžné příklady

### Zobrazení aktuální lokalizace
Chcete-li zobrazit aktuální nastavení lokalizace, použijte:

```bash
locale
```

### Zobrazení všech dostupných lokalizací
Pro zobrazení seznamu všech dostupných lokalizací v systému použijte:

```bash
locale -a
```

### Zobrazení mapování znaků
Pokud chcete zobrazit dostupná mapování znaků, použijte:

```bash
locale -m
```

### Zobrazení konkrétní informace o lokalizaci
Chcete-li zobrazit konkrétní informace o lokalizaci, například formát data, použijte:

```bash
locale -k LC_TIME
```

## Tipy
- Ujistěte se, že máte nainstalované potřebné lokalizace, aby příkaz `locale` mohl správně fungovat.
- Můžete změnit lokalizaci pro aktuální relaci pomocí příkazu `export`, například: `export LANG=cs_CZ.UTF-8`.
- Pro trvalé změny lokalizace upravte soubory jako `.bashrc` nebo `.profile` ve vašem domovském adresáři.