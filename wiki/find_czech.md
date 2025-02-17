# [Linux] Bash find použití: Hledání názvů souborů

## Přehled
Příkaz `find` slouží k vyhledávání souborů a adresářů v hierarchii souborového systému na základě různých kritérií, jako jsou název, typ, velikost nebo datum poslední změny.

## Použití
Základní syntaxe příkazu `find` je následující:

```
find [možnosti] [argumenty]
```

## Běžné možnosti
- `-name <název>`: Hledá soubory podle názvu.
- `-type <typ>`: Filtruje výsledky podle typu souboru (např. `f` pro soubory, `d` pro adresáře).
- `-size <velikost>`: Hledá soubory podle velikosti (např. `+100M` pro soubory větší než 100 MB).
- `-mtime <dny>`: Hledá soubory podle data poslední změny (např. `-mtime -7` pro soubory změněné v posledních 7 dnech).
- `-exec <příkaz> {} \;`: Provádí příkaz na nalezené soubory.

## Běžné příklady
- Hledání souboru s konkrétním názvem:
    ```bash
    find /cesta/k/adresáři -name "soubor.txt"
    ```

- Hledání všech adresářů:
    ```bash
    find /cesta/k/adresáři -type d
    ```

- Hledání souborů větších než 50 MB:
    ```bash
    find /cesta/k/adresáři -size +50M
    ```

- Hledání souborů změněných v posledních 10 dnech:
    ```bash
    find /cesta/k/adresáři -mtime -10
    ```

- Hledání a odstranění prázdných adresářů:
    ```bash
    find /cesta/k/adresáři -type d -empty -delete
    ```

## Tipy
- Používejte `-iname` místo `-name`, pokud chcete ignorovat velikost písmen při vyhledávání.
- Kombinujte více podmínek pomocí `-and` nebo `-or` pro složitější vyhledávání.
- Před provedením destruktivních operací (např. `-delete`) je dobré nejprve spustit příkaz s `-print`, abyste viděli, které soubory budou ovlivněny.