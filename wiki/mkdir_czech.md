# [Linux] Bash mkdir použití: Vytváření adresářů

## Přehled
Příkaz `mkdir` slouží k vytváření nových adresářů v systému. Je to základní nástroj pro organizaci souborů a složek v Linuxu a dalších Unixových systémech.

## Použití
Základní syntaxe příkazu je následující:

```bash
mkdir [možnosti] [argumenty]
```

## Běžné možnosti
- `-p`: Vytvoří rodičovské adresáře, pokud neexistují.
- `-v`: Zobrazí podrobnosti o vytvářených adresářích.
- `-m`: Nastaví oprávnění pro nově vytvořený adresář.

## Běžné příklady
1. Vytvoření jednoduchého adresáře:
   ```bash
   mkdir novy_adresar
   ```

2. Vytvoření více adresářů najednou:
   ```bash
   mkdir adresar1 adresar2 adresar3
   ```

3. Vytvoření adresáře a všech jeho rodičů:
   ```bash
   mkdir -p /cesta/k/adresari/novy_adresar
   ```

4. Vytvoření adresáře s konkrétními oprávněními:
   ```bash
   mkdir -m 755 novy_adresar
   ```

5. Zobrazení informací o vytvářeném adresáři:
   ```bash
   mkdir -v novy_adresar
   ```

## Tipy
- Při vytváření více adresářů najednou se ujistěte, že máte správná oprávnění pro všechny cílové umístění.
- Použití volby `-p` je užitečné, pokud si nejste jisti, zda rodičovské adresáře existují, což může ušetřit čas a úsilí.
- Pokud často vytváříte adresáře s určitými oprávněními, zvažte vytvoření aliasu pro příkaz `mkdir` s přednastavenými možnostmi.