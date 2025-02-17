# [Linux] Bash wget použití: Stahování souborů z webu

## Přehled
Příkaz `wget` je nástroj pro stahování souborů z webu. Umožňuje uživatelům stahovat soubory pomocí protokolů HTTP, HTTPS a FTP. Je to užitečný nástroj pro automatizaci stahování a může být použit pro stahování jednotlivých souborů nebo celých webových stránek.

## Použití
Základní syntaxe příkazu wget je následující:

```bash
wget [možnosti] [argumenty]
```

## Běžné možnosti
- `-O [soubor]`: Umožňuje specifikovat název souboru, do kterého bude stažený obsah uložen.
- `-c`: Pokračuje v přerušeném stahování.
- `-r`: Stahuje soubory rekurzivně, což znamená, že stáhne všechny související soubory.
- `-p`: Stahuje všechny potřebné soubory pro zobrazení HTML stránky (např. obrázky, CSS).
- `--limit-rate=[rychlost]`: Omezuje rychlost stahování na zadanou hodnotu.

## Běžné příklady
1. **Stáhnout soubor:**
   ```bash
   wget http://example.com/soubor.zip
   ```

2. **Stáhnout soubor a uložit ho pod jiným názvem:**
   ```bash
   wget -O novy_nazev.zip http://example.com/soubor.zip
   ```

3. **Pokračovat v přerušeném stahování:**
   ```bash
   wget -c http://example.com/soubor.zip
   ```

4. **Rekurzivní stahování celé webové stránky:**
   ```bash
   wget -r http://example.com/
   ```

5. **Stáhnout stránku a všechny potřebné soubory:**
   ```bash
   wget -p http://example.com/
   ```

## Tipy
- Při stahování velkých souborů zvažte použití možnosti `--limit-rate`, abyste nezatěžovali síť.
- Pokud stahujete více souborů, můžete je uvést v textovém souboru a použít `-i [soubor]` pro hromadné stahování.
- Vždy zkontrolujte, zda máte povolení k stahování obsahu z webu, abyste se vyhnuli porušení autorských práv.