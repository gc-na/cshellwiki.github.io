# [Linux] Bash lsof Použití: Zobrazení otevřených souborů a procesů

## Přehled
Příkaz `lsof` (List Open Files) slouží k zobrazení seznamu otevřených souborů a procesů, které je používají. Tento nástroj je užitečný pro diagnostiku problémů se soubory a sledování, které procesy mají přístup k určitým souborům nebo portům.

## Použití
Základní syntaxe příkazu `lsof` je následující:

```bash
lsof [možnosti] [argumenty]
```

## Běžné možnosti
- `-a` : Kombinuje další možnosti (AND).
- `-c <název>` : Zobrazí pouze soubory otevřené procesy s daným názvem.
- `-u <uživatel>` : Zobrazí soubory otevřené procesy patřící danému uživateli.
- `-p <PID>` : Zobrazí soubory otevřené procesem s daným identifikátorem procesu (PID).
- `+D <adresář>` : Zobrazí soubory otevřené v daném adresáři a jeho podadresářích.

## Běžné příklady
1. Zobrazit všechny otevřené soubory:
   ```bash
   lsof
   ```

2. Zobrazit soubory otevřené konkrétním uživatelem:
   ```bash
   lsof -u username
   ```

3. Zobrazit soubory otevřené procesem s konkrétním PID:
   ```bash
   lsof -p 1234
   ```

4. Zobrazit všechny soubory otevřené v konkrétním adresáři:
   ```bash
   lsof +D /cesta/k/adresáři
   ```

5. Zobrazit síťové spojení a otevřené porty:
   ```bash
   lsof -i
   ```

## Tipy
- Používejte `sudo` pro zobrazení souborů otevřených procesy, které patří jiným uživatelům.
- Kombinujte možnosti pro specifické dotazy, například `lsof -u username -p 1234` pro zúžení výsledků.
- Pravidelně kontrolujte otevřené soubory, abyste předešli problémům s nedostatkem systémových prostředků.