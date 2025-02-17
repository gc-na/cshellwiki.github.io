# [Linux] Bash test použití: Ověření podmínek

## Přehled
Příkaz `test` v Bash slouží k vyhodnocení podmínek a vrací statusový kód na základě výsledku. Je často používán v podmínkových výrazech, aby se zjistilo, zda jsou splněny určité podmínky, například existence souboru nebo porovnání hodnot.

## Použití
Základní syntaxe příkazu `test` je následující:

```bash
test [možnosti] [argumenty]
```

## Běžné možnosti
- `-e [soubor]`: Ověří, zda soubor existuje.
- `-f [soubor]`: Ověří, zda je soubor běžný soubor.
- `-d [adresář]`: Ověří, zda je zadaný argument adresář.
- `-z [řetězec]`: Ověří, zda je řetězec prázdný.
- `-n [řetězec]`: Ověří, zda je řetězec neprázdný.
- `[hodnota1] -eq [hodnota2]`: Ověří, zda jsou dvě hodnoty rovny.
- `[hodnota1] -lt [hodnota2]`: Ověří, zda je první hodnota menší než druhá.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `test`:

1. Ověření existence souboru:
   ```bash
   test -e soubor.txt && echo "Soubor existuje."
   ```

2. Ověření, zda je zadaný argument adresář:
   ```bash
   test -d /cesta/k/adresáři && echo "Je to adresář."
   ```

3. Ověření, zda je proměnná prázdná:
   ```bash
   VAR=""
   test -z "$VAR" && echo "Proměnná je prázdná."
   ```

4. Porovnání dvou čísel:
   ```bash
   A=5
   B=10
   test $A -lt $B && echo "$A je menší než $B."
   ```

## Tipy
- Používejte `[` a `]` jako alternativu k `test`, což může zlepšit čitelnost:
  ```bash
  [ -e soubor.txt ] && echo "Soubor existuje."
  ```

- Vždy uzavírejte proměnné do uvozovek, aby se předešlo chybám při porovnávání prázdných nebo neexistujících hodnot.

- Při použití v podmínkových příkazech, jako je `if`, je `test` často implicitně volán, což zjednodušuje syntaxi:
  ```bash
  if test -f soubor.txt; then
      echo "Soubor je běžný soubor."
  fi
  ```