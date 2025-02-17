# [Linux] Bash 7z použití: Komprimace a dekomprimace souborů

## Přehled
Příkaz `7z` je součástí archivačního nástroje 7-Zip, který slouží k vytváření a extrakci archivů různých formátů. Tento nástroj je známý svou vysokou kompresní účinností a podporou mnoha formátů souborů.

## Použití
Základní syntaxe příkazu `7z` je následující:

```
7z [možnosti] [argumenty]
```

## Běžné možnosti
- `a`: Přidat soubory do archivu.
- `x`: Extrahovat soubory z archivu.
- `l`: Vypsat obsah archivu.
- `d`: Smazat soubory z archivu.
- `t`: Otestovat integritu archivu.

## Běžné příklady
### Vytvoření archivu
Chcete-li vytvořit archiv s názvem `moje_soubory.7z` a přidat do něj všechny soubory z aktuálního adresáře, použijte:

```bash
7z a moje_soubory.7z *
```

### Extrakce archivu
Pro extrakci obsahu archivu `moje_soubory.7z` do aktuálního adresáře použijte:

```bash
7z x moje_soubory.7z
```

### Vypsání obsahu archivu
Chcete-li zobrazit seznam souborů v archivu `moje_soubory.7z`, použijte:

```bash
7z l moje_soubory.7z
```

### Smazání souboru z archivu
Pokud chcete odstranit soubor `soubor.txt` z archivu `moje_soubory.7z`, použijte:

```bash
7z d moje_soubory.7z soubor.txt
```

## Tipy
- Při komprimaci velkých souborů zvažte použití různých úrovní komprese pomocí volby `-mx`, kde `x` je číslo od 0 (bez komprese) do 9 (maximální komprese).
- Vždy testujte integritu archivu po jeho vytvoření pomocí volby `t`, abyste se ujistili, že není poškozený.
- Pro zrychlení procesu komprese můžete použít více vláken pomocí volby `-mmt`.

Tento nástroj je velmi užitečný pro správu souborů a archivaci, a jeho použití může výrazně usnadnit práci s daty.