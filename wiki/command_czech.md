# [Linux] Bash příkaz cp: kopírování souborů a adresářů

## Přehled
Příkaz `cp` slouží k kopírování souborů a adresářů v systému Linux. Umožňuje uživatelům snadno duplikovat soubory nebo celé adresářové struktury.

## Použití
Základní syntaxe příkazu `cp` je následující:

```
cp [možnosti] [zdroj] [cílový]
```

## Běžné možnosti
- `-r`: Kopíruje adresáře rekurzivně.
- `-i`: Před přepsáním existujícího souboru se zeptá na potvrzení.
- `-u`: Kopíruje pouze soubory, které jsou novější než cílové soubory nebo které neexistují.
- `-v`: Zobrazí podrobnosti o tom, co se kopíruje.

## Běžné příklady
1. **Kopírování souboru do jiného umístění:**
   ```bash
   cp soubor.txt /cesta/k/cilovemu/
   ```

2. **Kopírování adresáře rekurzivně:**
   ```bash
   cp -r adresar/ /cesta/k/cilovemu/
   ```

3. **Kopírování souboru s potvrzením:**
   ```bash
   cp -i soubor.txt /cesta/k/cilovemu/
   ```

4. **Kopírování pouze novějších souborů:**
   ```bash
   cp -u soubor.txt /cesta/k/cilovemu/
   ```

5. **Kopírování souboru a zobrazení podrobností:**
   ```bash
   cp -v soubor.txt /cesta/k/cilovemu/
   ```

## Tipy
- Při kopírování velkých adresářů použijte možnost `-v`, abyste viděli průběh operace.
- Pokud často kopírujete soubory, které mohou existovat v cílovém umístění, zvažte použití možnosti `-i`, abyste se vyhnuli nechtěnému přepsání.
- Pro efektivní práci s více soubory můžete použít zástupné znaky, například `*.txt` pro kopírování všech textových souborů.