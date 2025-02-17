# [Linux] Bash typ příkazu: Zjistit typ příkazu

## Přehled
Příkaz `type` se používá k určení typu příkazu, který je zadán v Bash. Může to být interní příkaz shellu, externí program, alias nebo funkce. Tento příkaz je užitečný pro diagnostiku a porozumění, jak Bash interpretuje různé příkazy.

## Použití
Základní syntaxe příkazu `type` je následující:

```bash
type [options] [arguments]
```

## Běžné možnosti
- `-a`: Zobrazí všechny umístění příkazu, pokud existuje více verzí.
- `-p`: Zobrazí pouze cestu k externímu příkazu.
- `-t`: Zobrazí typ příkazu (např. alias, function, builtin, file).
- `-f`: Zobrazí pouze externí příkazy, ignoruje aliasy a funkce.

## Běžné příklady

1. Zjistit typ příkazu `ls`:
   ```bash
   type ls
   ```

2. Zjistit typ aliasu `ll`:
   ```bash
   alias ll='ls -l'
   type ll
   ```

3. Zobrazit všechny verze příkazu `echo`:
   ```bash
   type -a echo
   ```

4. Zjistit pouze cestu k externímu příkazu `grep`:
   ```bash
   type -p grep
   ```

5. Zjistit typ příkazu `cd`:
   ```bash
   type -t cd
   ```

## Tipy
- Používejte `type` k rychlému ověření, zda je příkaz interní nebo externí, což může pomoci při ladění skriptů.
- Pokud máte aliasy, které se chovají jako příkazy, použijte `type -a` pro zobrazení všech variant.
- Pro rychlé zjištění, zda je příkaz funkce, použijte `type -t`, což vám ušetří čas při hledání problémů ve skriptech.