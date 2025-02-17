# [Linux] Bash zip použití: Komprimace souborů a adresářů

## Přehled
Příkaz `zip` slouží k vytváření komprimovaných archivů ve formátu ZIP. Umožňuje uživatelům zabalit jeden nebo více souborů a adresářů do jednoho souboru, čímž se šetří místo na disku a usnadňuje přenos dat.

## Použití
Základní syntaxe příkazu `zip` je následující:

```bash
zip [možnosti] [název_archivu.zip] [soubory/adresáře]
```

## Běžné možnosti
- `-r`: Rekurzivně zahrnout adresáře.
- `-e`: Šifrovat obsah archivu.
- `-9`: Použít maximální úroveň komprese.
- `-q`: Tichý režim, bez výstupu na obrazovku.

## Běžné příklady
1. **Zabalení jednotlivého souboru:**
   ```bash
   zip archiv.zip soubor.txt
   ```

2. **Zabalení více souborů:**
   ```bash
   zip archiv.zip soubor1.txt soubor2.txt soubor3.txt
   ```

3. **Zabalení celého adresáře:**
   ```bash
   zip -r archiv.zip adresar/
   ```

4. **Zabalení souborů s maximální kompresí:**
   ```bash
   zip -9 archiv.zip soubor.txt
   ```

5. **Zabalení souborů a šifrování archivu:**
   ```bash
   zip -e archiv.zip soubor.txt
   ```

## Tipy
- Před komprimací zkontrolujte, zda máte dostatek místa na disku pro vytvoření archivu.
- Používejte možnost `-r` pro zahrnutí celých adresářů, abyste se vyhnuli zdlouhavému zadávání jednotlivých souborů.
- Při šifrování archivu nezapomeňte si zapamatovat heslo, protože bez něj nebude možné obsah dekomprimovat.