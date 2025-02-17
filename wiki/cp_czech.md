# [Linux] Bash cp použití: Kopírování souborů a adresářů

## Přehled
Příkaz `cp` slouží k kopírování souborů a adresářů v systému Linux. Umožňuje uživatelům snadno duplikovat soubory na stejném nebo jiném místě v souborovém systému.

## Použití
Základní syntaxe příkazu `cp` je následující:

```bash
cp [možnosti] [argumenty]
```

## Běžné možnosti
- `-r`: Rekurzivní kopírování, používá se pro kopírování adresářů a jejich obsahu.
- `-i`: Interaktivní režim, který se ptá na potvrzení před přepsáním existujícího souboru.
- `-u`: Kopíruje pouze soubory, které jsou novější než cílové soubory nebo které neexistují.
- `-v`: Verbózní režim, který zobrazuje podrobnosti o tom, co se kopíruje.

## Běžné příklady
Kopírování souboru `soubor.txt` do cílového umístění `novy_soubor.txt`:

```bash
cp soubor.txt novy_soubor.txt
```

Kopírování adresáře `adresar` do cílového umístění `novy_adresar`:

```bash
cp -r adresar novy_adresar
```

Kopírování souboru s potvrzením před přepsáním:

```bash
cp -i soubor.txt novy_soubor.txt
```

Kopírování pouze novějších souborů:

```bash
cp -u soubor.txt novy_soubor.txt
```

## Tipy
- Před použitím příkazu `cp` se ujistěte, že máte správná oprávnění pro čtení a zápis v cílovém umístění.
- Používejte volbu `-v`, abyste měli přehled o tom, co se kopíruje, zejména při kopírování více souborů nebo adresářů.
- Pokud kopírujete velké množství dat, zvažte použití příkazu `rsync`, který je efektivnější pro synchronizaci souborů.