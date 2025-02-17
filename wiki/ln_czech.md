# [Linux] Bash ln použití: Vytváření odkazů na soubory

## Přehled
Příkaz `ln` slouží k vytváření odkazů na soubory v systému. Může vytvářet jak tvrdé odkazy, které sdílejí stejný inode, tak symbolické odkazy, které fungují jako zástupci pro jiné soubory nebo adresáře.

## Použití
Základní syntaxe příkazu `ln` je následující:

```bash
ln [možnosti] [argumenty]
```

## Běžné možnosti
- `-s`: Vytvoří symbolický odkaz místo tvrdého odkazu.
- `-f`: Přepíše existující soubor bez varování.
- `-n`: Pokud cílový odkaz již existuje, nebude přepsán, pokud je to možné.
- `-v`: Zobrazí podrobnosti o vytvářených odkazech.

## Běžné příklady
### Vytvoření tvrdého odkazu
```bash
ln soubor.txt odkaz.txt
```
Tento příkaz vytvoří tvrdý odkaz `odkaz.txt`, který ukazuje na `soubor.txt`.

### Vytvoření symbolického odkazu
```bash
ln -s soubor.txt symlink.txt
```
Tento příkaz vytvoří symbolický odkaz `symlink.txt`, který odkazuje na `soubor.txt`.

### Přepsání existujícího odkazu
```bash
ln -sf novy_soubor.txt odkaz.txt
```
Tento příkaz přepíše existující odkaz `odkaz.txt` a vytvoří nový odkaz na `novy_soubor.txt`.

### Vytvoření symbolického odkazu na adresář
```bash
ln -s /cesta/k/adresari odkaz_na_adresar
```
Tento příkaz vytvoří symbolický odkaz na adresář.

## Tipy
- Používejte symbolické odkazy pro odkazy na adresáře nebo soubory, které se mohou měnit, protože se snadno aktualizují.
- Při vytváření tvrdých odkazů si dejte pozor, že nemohou odkazovat na adresáře a nemohou být vytvořeny na různých souborových systémech.
- Pokud potřebujete přepsat existující odkazy, použijte možnost `-f`, abyste se vyhnuli chybovým hlášením.