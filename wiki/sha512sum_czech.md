# [Linux] Bash sha512sum použití: Vytváření a ověřování SHA-512 hashů

## Přehled
Příkaz `sha512sum` slouží k vytváření a ověřování hashů pomocí algoritmu SHA-512. Tento příkaz je užitečný pro zajištění integrity souborů, protože generuje jedinečný otisk dat, který lze použít k ověření, zda byl soubor změněn.

## Použití
Základní syntaxe příkazu `sha512sum` je následující:

```
sha512sum [možnosti] [argumenty]
```

## Běžné možnosti
- `-b`: Zpracovává binární soubory.
- `-c`: Ověřuje soubory podle zadaného hash souboru.
- `-h`: Zobrazí nápovědu k příkazu.
- `--tag`: Vytvoří výstup v "BSD" formátu.

## Běžné příklady

### Vytvoření SHA-512 hashe souboru
Pro vygenerování SHA-512 hashe souboru `soubor.txt` použijte následující příkaz:

```bash
sha512sum soubor.txt
```

### Uložení hashe do souboru
Pokud chcete uložit hash do souboru `hash.txt`, můžete použít:

```bash
sha512sum soubor.txt > hash.txt
```

### Ověření souboru pomocí hash souboru
Pokud máte soubor s hashem, například `hash.txt`, a chcete ověřit integritu souboru `soubor.txt`, použijte:

```bash
sha512sum -c hash.txt
```

### Vytvoření hashe pro více souborů
Chcete-li vygenerovat hashe pro více souborů najednou, můžete je uvést za sebe:

```bash
sha512sum soubor1.txt soubor2.txt
```

## Tipy
- Při ověřování hashů vždy používejte soubor s hashem, abyste zajistili správnost.
- Ukládejte hashe pro důležité soubory, abyste mohli snadno zkontrolovat jejich integritu v budoucnu.
- Používejte možnost `-b` pro binární soubory, abyste se vyhnuli problémům s kódováním.