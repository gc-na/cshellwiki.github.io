# [Linux] Bash tr použití: Převod a nahrazení znaků

## Přehled
Příkaz `tr` (translate) se používá v Bash pro převod nebo nahrazení znaků v textovém vstupu. Může být užitečný pro úpravu textu, jako je změna malých písmen na velká, nebo pro odstranění nežádoucích znaků.

## Použití
Základní syntaxe příkazu `tr` je následující:

```bash
tr [možnosti] [argumenty]
```

## Běžné možnosti
- `-d`: Odstraní zadané znaky.
- `-s`: Zkrátí opakující se znaky na jeden.
- `-c`: Použije komplement zadaných znaků.

## Běžné příklady

1. **Převod malých písmen na velká:**

```bash
echo "ahoj světe" | tr 'a-z' 'A-Z'
```

Tento příkaz převede text "ahoj světe" na "AHOJ SVĚTE".

2. **Odstranění číslic:**

```bash
echo "abc123def456" | tr -d '0-9'
```

Tento příkaz odstraní všechny číslice z textu, výsledkem bude "abcdef".

3. **Zkrácení opakujících se mezer:**

```bash
echo "Toto   je   příklad." | tr -s ' '
```

Tento příkaz zkrátí více mezer na jednu, výsledkem bude "Toto je příklad."

4. **Nahrazení znaků:**

```bash
echo "jablko, hruška, banán" | tr ',' ';'
```

Tento příkaz nahradí čárky středníky, výsledkem bude "jablko; hruška; banán".

## Tipy
- Při použití `tr` s velkými objemy dat je dobré použít příkaz v kombinaci s dalšími nástroji, jako je `grep` nebo `sed`, pro efektivnější zpracování textu.
- Vždy testujte příkazy na malých vzorcích dat, než je použijete na větší soubory, abyste se ujistili, že dosáhnete požadovaného výsledku.