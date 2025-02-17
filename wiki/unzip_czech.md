# [Linux] Bash unzip použití: Rozbalení zip souborů

## Přehled
Příkaz `unzip` slouží k rozbalení souborů ze zip archivu. Tento nástroj je užitečný pro extrakci souborů, které byly komprimovány do formátu ZIP, což šetří místo na disku a usnadňuje přenos dat.

## Použití
Základní syntaxe příkazu `unzip` je následující:

```bash
unzip [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Zobrazí seznam souborů v archivu bez jejich rozbalení.
- `-d [adresář]`: Určuje cílový adresář, do kterého budou soubory rozbaleny.
- `-o`: Přepíše existující soubory bez dotazu.
- `-q`: Potlačí výstup, takže se zobrazí pouze chybové zprávy.

## Běžné příklady
- Rozbalení zip souboru do aktuálního adresáře:

```bash
unzip soubor.zip
```

- Rozbalení zip souboru do specifického adresáře:

```bash
unzip soubor.zip -d /cesta/k/adresáři
```

- Zobrazení obsahu zip souboru bez jeho rozbalení:

```bash
unzip -l soubor.zip
```

- Rozbalení zip souboru a přepsání existujících souborů bez dotazu:

```bash
unzip -o soubor.zip
```

## Tipy
- Před rozbalením zip souboru se ujistěte, že máte dostatek volného místa na disku.
- Používejte možnost `-d`, abyste měli přehled o tom, kam soubory rozbalujete, zejména pokud pracujete s více archivy.
- Pokud potřebujete rozbalit více zip souborů najednou, můžete použít zástupné znaky, například `unzip '*.zip'`.