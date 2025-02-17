# [Linux] Bash end použití: Zobrazí konec souboru

## Přehled
Příkaz `end` v Bash se používá k zobrazení posledních několika řádků textového souboru. Je užitečný pro rychlé prohlížení obsahu souboru, zejména pokud chcete vidět poslední záznamy bez nutnosti procházet celý soubor.

## Použití
Základní syntaxe příkazu je následující:

```
end [možnosti] [argumenty]
```

## Běžné možnosti
- `-n [číslo]`: Určuje počet řádků, které se mají zobrazit na konci souboru. Výchozí hodnota je 10.
- `-f`: Sleduje soubor a zobrazuje nové řádky, jakmile jsou přidány (užitečné pro logy).
- `-q`: Potlačuje výstup názvu souboru.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `end`:

1. Zobrazení posledních 10 řádků souboru `log.txt`:
   ```bash
   end log.txt
   ```

2. Zobrazení posledních 5 řádků souboru `data.txt`:
   ```bash
   end -n 5 data.txt
   ```

3. Sledování souboru `server.log` pro nové řádky:
   ```bash
   end -f server.log
   ```

4. Zobrazení posledních 20 řádků souboru `output.txt` bez názvu souboru:
   ```bash
   end -n 20 -q output.txt
   ```

## Tipy
- Pokud často potřebujete sledovat logy, zvažte použití příkazu `end -f` pro automatické zobrazení nových záznamů.
- Při práci s velkými soubory použijte možnost `-n`, abyste omezili množství zobrazených dat a zaměřili se pouze na to, co potřebujete.
- Kombinujte příkaz `end` s dalšími příkazy, jako je `grep`, pro filtrování specifických řádků, které vás zajímají.