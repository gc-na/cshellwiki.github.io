# [Linux] Bash csplit použití: Rozdělení souboru na části

## Přehled
Příkaz `csplit` slouží k rozdělení textového souboru na menší části na základě specifikovaných vzorů nebo počtu řádků. Tento nástroj je užitečný, když potřebujete analyzovat nebo zpracovávat velké soubory po částech.

## Použití
Základní syntaxe příkazu `csplit` je následující:

```bash
csplit [možnosti] [argumenty]
```

## Běžné možnosti
- `-f PREFIX`: Určuje předponu pro názvy výstupních souborů.
- `-n NUM`: Nastavuje počet číslic pro číslování výstupních souborů.
- `-b SUFFIX`: Určuje příponu pro výstupní soubory.
- `-k`: Zachovává soubory, i když dojde k chybě.

## Běžné příklady
1. Rozdělení souboru na každých 100 řádků:
   ```bash
   csplit myfile.txt 100
   ```

2. Rozdělení souboru na základě vzoru (např. každé výskyt slova "START"):
   ```bash
   csplit myfile.txt /START/
   ```

3. Použití vlastní předpony pro výstupní soubory:
   ```bash
   csplit -f part_ myfile.txt 100
   ```

4. Rozdělení souboru na části a zachování souborů i při chybě:
   ```bash
   csplit -k myfile.txt /ERROR/
   ```

## Tipy
- Při práci s velkými soubory je dobré použít možnost `-n`, aby bylo číslování výstupních souborů přehledné.
- Pokud potřebujete rozdělit soubor na základě více vzorů, můžete je zadat za sebou.
- Ujistěte se, že máte dostatek místa na disku, protože každý výstupní soubor zabere místo.