# [Linux] Bash rmdir použití: Odstranění prázdných adresářů

## Přehled
Příkaz `rmdir` slouží k odstranění prázdných adresářů v systému. Pokud se pokusíte odstranit adresář, který obsahuje soubory nebo jiné adresáře, příkaz selže.

## Použití
Základní syntaxe příkazu je následující:

```bash
rmdir [možnosti] [argumenty]
```

## Běžné možnosti
- `--ignore-fail-on-non-empty`: Tato možnost způsobí, že příkaz nebude hlásit chybu, pokud se pokusíte odstranit neprázdný adresář.
- `--verbose`: Zobrazí podrobnosti o operaci, kterou příkaz provádí.
- `--help`: Zobrazí nápovědu k příkazu a jeho možnostem.

## Běžné příklady
1. Odstranění prázdného adresáře:
   ```bash
   rmdir /cesta/k/adresari
   ```

2. Odstranění více prázdných adresářů najednou:
   ```bash
   rmdir /cesta/k/adresari1 /cesta/k/adresari2
   ```

3. Použití možnosti `--verbose` pro zobrazení podrobností:
   ```bash
   rmdir --verbose /cesta/k/adresari
   ```

4. Ignorování chyb při pokusu o odstranění neprázdného adresáře:
   ```bash
   rmdir --ignore-fail-on-non-empty /cesta/k/adresari
   ```

## Tipy
- Před použitím příkazu `rmdir` se ujistěte, že adresář je skutečně prázdný, abyste se vyhnuli chybám.
- Pokud potřebujete odstranit adresář, který obsahuje soubory, použijte příkaz `rm -r` místo `rmdir`.
- Vždy můžete použít možnost `--verbose`, abyste měli přehled o tom, co se děje během operace.