# [Linux] Bash mv použití: Přesouvání a přejmenovávání souborů

## Přehled
Příkaz `mv` se používá v Bash pro přesouvání a přejmenovávání souborů a adresářů. Umožňuje uživatelům snadno organizovat soubory v systému souborů.

## Použití
Základní syntaxe příkazu `mv` je následující:

```bash
mv [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Interaktivní režim, který se ptá na potvrzení před přepsáním existujícího souboru.
- `-u`: Přesune pouze soubory, které jsou novější než cílové soubory nebo pokud cílové soubory neexistují.
- `-v`: Zobrazí podrobnosti o tom, co se přesouvá, a kam.

## Běžné příklady
1. **Přejmenování souboru:**
   ```bash
   mv starý_název.txt nový_název.txt
   ```

2. **Přesunutí souboru do jiného adresáře:**
   ```bash
   mv soubor.txt /cesta/k/adresáři/
   ```

3. **Přesunutí více souborů do jiného adresáře:**
   ```bash
   mv soubor1.txt soubor2.txt /cesta/k/adresáři/
   ```

4. **Použití interaktivního režimu:**
   ```bash
   mv -i soubor.txt /cesta/k/adresáři/
   ```

5. **Přesunutí souboru pouze pokud je novější:**
   ```bash
   mv -u soubor.txt /cesta/k/adresáři/
   ```

## Tipy
- Před použitím příkazu `mv` se ujistěte, že máte správné cesty k souborům a adresářům, abyste předešli nechtěnému přepsání.
- Používejte možnost `-i`, pokud pracujete s důležitými soubory, abyste se vyhnuli ztrátě dat.
- Pro lepší přehlednost můžete použít možnost `-v`, abyste viděli, co se přesouvá.