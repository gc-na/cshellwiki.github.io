# [Linux] Bash stty použití: Nastavení a kontrola terminálových atributů

## Přehled
Příkaz `stty` se používá k nastavení a kontrole atributů terminálu. Umožňuje uživatelům měnit chování terminálu, jako je například nastavení klávesových zkratek, ovládání vstupu a výstupu a další vlastnosti.

## Použití
Základní syntaxe příkazu je následující:

```bash
stty [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechny aktuální nastavení terminálu.
- `-g`: Vytvoří řetězec, který lze použít k obnovení aktuálního nastavení.
- `erase`: Nastaví znak pro mazání (např. `stty erase ^H` pro backspace).
- `intr`: Nastaví znak pro přerušení (např. `stty intr ^C` pro Ctrl+C).
- `echo`: Zapne nebo vypne echo vstupu.

## Běžné příklady
- Zobrazit všechna aktuální nastavení terminálu:

```bash
stty -a
```

- Nastavit znak pro mazání na backspace:

```bash
stty erase ^H
```

- Nastavit znak pro přerušení na Ctrl+C:

```bash
stty intr ^C
```

- Vypnout echo vstupu:

```bash
stty -echo
```

- Zapnout echo vstupu:

```bash
stty echo
```

## Tipy
- Před provedením změn pomocí `stty` je dobré si uložit aktuální nastavení pomocí `stty -g`, abyste je mohli snadno obnovit.
- Používejte `stty` v interaktivních shellových skriptech pro přizpůsobení uživatelského rozhraní.
- Pokud se něco pokazí, můžete použít `stty sane` k obnovení výchozího nastavení terminálu.