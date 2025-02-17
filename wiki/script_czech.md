# [Linux] Bash skript použití: Záznam terminálových sezení

## Přehled
Příkaz `script` slouží k zaznamenávání terminálových sezení do souboru. Je užitečný pro uchování historie příkazů a výstupů, což může být užitečné pro dokumentaci nebo sdílení informací.

## Použití
Základní syntaxe příkazu je následující:

```bash
script [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Přidá výstup do existujícího souboru místo jeho přepsání.
- `-q`: Potlačí výstup informací o zahájení a ukončení záznamu.
- `-t`: Zaznamenává časové údaje o provedených příkazech.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `script`:

1. Základní záznam do souboru `session.log`:
   ```bash
   script session.log
   ```

2. Záznam se potlačením informačního výstupu:
   ```bash
   script -q session.log
   ```

3. Přidání výstupu do již existujícího souboru:
   ```bash
   script -a session.log
   ```

4. Záznam s časovými údaji:
   ```bash
   script -t session.log
   ```

## Tipy
- Před zahájením záznamu se ujistěte, že máte dostatek místa na disku, aby se předešlo problémům s ukládáním.
- Po ukončení záznamu můžete soubor otevřít v textovém editoru pro prohlížení nebo analýzu.
- Používejte volbu `-q`, pokud nechcete, aby se na obrazovce zobrazovaly informace o záznamu, což může být užitečné při automatizaci skriptů.