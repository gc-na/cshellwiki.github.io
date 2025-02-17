# [Linux] Bash fg použití: Obnovení pozastaveného procesu na popředí

## Přehled
Příkaz `fg` v Bash slouží k obnovení pozastaveného procesu a jeho přesunu na popředí terminálu. To umožňuje uživatelům interagovat s procesem, který byl dříve pozastaven pomocí příkazu `Ctrl+Z`.

## Použití
Základní syntaxe příkazu `fg` je následující:

```bash
fg [možnosti] [argumenty]
```

## Běžné možnosti
- `job_spec`: Určuje specifický úkol, který chcete obnovit. Může to být číslo úkolu (např. `%1`) nebo název procesu.
- `-n`: Přeskočí na další úkol, pokud je aktuální úkol pozastaven.

## Běžné příklady
1. **Obnovení posledního pozastaveného procesu:**
   ```bash
   fg
   ```

2. **Obnovení specifického procesu podle čísla úkolu:**
   ```bash
   fg %1
   ```

3. **Obnovení procesu podle názvu:**
   ```bash
   fg %názov_procesu
   ```

4. **Obnovení dalšího pozastaveného procesu:**
   ```bash
   fg -n
   ```

## Tipy
- Pokud máte více pozastavených procesů, můžete použít příkaz `jobs` pro zobrazení seznamu a jejich čísel.
- Při práci s více procesy buďte opatrní, abyste nezaměnili čísla úkolů, což může vést k nechtěnému obnovení nesprávného procesu.
- Příkaz `fg` je užitečný při práci s dlouhotrvajícími úkoly, které potřebujete dočasně pozastavit a později obnovit.