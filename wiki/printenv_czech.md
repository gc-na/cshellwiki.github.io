# [Linux] Bash printenv použití: Zobrazení proměnných prostředí

## Přehled
Příkaz `printenv` slouží k zobrazení hodnot proměnných prostředí v systému. Umožňuje uživatelům rychle zjistit, jaké proměnné jsou aktuálně nastavené a jaké mají hodnoty.

## Použití
Základní syntaxe příkazu je následující:

```bash
printenv [možnosti] [argumenty]
```

## Běžné možnosti
- `-0`, `--null`: Odděluje výstup nulovými bajty místo nových řádků.
- `VARIABLE`: Pokud zadáte název proměnné, `printenv` zobrazí pouze její hodnotu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `printenv`:

1. Zobrazení všech proměnných prostředí:
   ```bash
   printenv
   ```

2. Zobrazení konkrétní proměnné prostředí, například `HOME`:
   ```bash
   printenv HOME
   ```

3. Zobrazení proměnných prostředí s nulovými bajty jako oddělovači:
   ```bash
   printenv -0
   ```

## Tipy
- Používejte `printenv` v kombinaci s dalšími příkazy, jako je `grep`, pro filtrování výsledků. Například:
  ```bash
  printenv | grep PATH
  ```
- Pokud potřebujete zjistit více o konkrétní proměnné, můžete použít příkaz `echo`, například:
  ```bash
  echo $USER
  ```
- Pamatujte, že `printenv` nezobrazuje proměnné, které nejsou nastavené. Pokud proměnná neexistuje, nebude v výstupu.