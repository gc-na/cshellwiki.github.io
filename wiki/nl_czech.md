# [Linux] Bash nl použití: Číslování řádků v textových souborech

## Přehled
Příkaz `nl` slouží k číslování řádků v textových souborech. Umožňuje uživatelům přidat čísla řádků před každý řádek textu, což může být užitečné pro zvýšení přehlednosti a organizace obsahu.

## Použití
Základní syntaxe příkazu `nl` je následující:

```bash
nl [možnosti] [argumenty]
```

## Běžné možnosti
- `-b` : Určuje, jakým způsobem se budou číslovat řádky (např. `-b a` pro číslování všech řádků).
- `-n` : Určuje formát číslování (např. `-n ln` pro levé zarovnání).
- `-w` : Nastavuje šířku čísel (např. `-w 4` pro čtyřmístná čísla).
- `-s` : Určuje oddělovač mezi číslem řádku a textem (např. `-s .` pro tečku jako oddělovač).

## Běžné příklady
1. Číslování všech řádků v souboru `soubor.txt`:
   ```bash
   nl soubor.txt
   ```

2. Číslování pouze neprazdných řádků:
   ```bash
   nl -b t soubor.txt
   ```

3. Číslování řádků s čtyřmístnými čísly:
   ```bash
   nl -w 4 soubor.txt
   ```

4. Použití tečky jako oddělovače:
   ```bash
   nl -s . soubor.txt
   ```

## Tipy
- Pokud potřebujete číslovat více souborů najednou, můžete je uvést za sebe:
  ```bash
  nl soubor1.txt soubor2.txt
  ```
- Pro lepší čitelnost můžete kombinovat různé možnosti, například:
  ```bash
  nl -b a -w 3 -s ": " soubor.txt
  ```
- Vždy si můžete prohlédnout nápovědu k příkazu `nl` pomocí:
  ```bash
  man nl
  ```