# [Linux] Bash crontab použití: Naplánování úloh

## Přehled
Příkaz `crontab` slouží k plánování automatického spouštění skriptů nebo příkazů v pravidelných intervalech na Unixových systémech. Umožňuje uživatelům definovat úlohy, které se mají vykonávat v konkrétní časy nebo intervaly.

## Použití
Základní syntaxe příkazu `crontab` je následující:

```bash
crontab [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Otevře aktuální crontab pro úpravy v výchozím textovém editoru.
- `-l`: Zobrazí aktuální crontab pro uživatele.
- `-r`: Odstraní aktuální crontab pro uživatele.
- `-i`: Potvrzení před odstraněním crontab (používá se s `-r`).

## Běžné příklady
1. **Zobrazení aktuálního crontab**:
   ```bash
   crontab -l
   ```

2. **Úprava crontab**:
   ```bash
   crontab -e
   ```

3. **Naplánování úlohy pro spuštění skriptu každou hodinu**:
   ```bash
   0 * * * * /cesta/k/vašemu/skriptu.sh
   ```

4. **Naplánování úlohy pro spuštění příkazu každý den v 5:30 ráno**:
   ```bash
   30 5 * * * /usr/bin/somecommand
   ```

5. **Odstranění crontab**:
   ```bash
   crontab -r
   ```

## Tipy
- Ujistěte se, že skripty, které plánujete spouštět, mají správná oprávnění k provádění.
- Používejte absolutní cesty k souborům a skriptům, aby se předešlo problémům s cestami.
- Zkontrolujte logy, pokud úlohy nefungují podle očekávání, abyste zjistili případné chyby.