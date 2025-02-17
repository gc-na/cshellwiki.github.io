# [Linux] Bash sftp použití: Přenos souborů přes SSH

## Přehled
Příkaz `sftp` (Secure File Transfer Protocol) slouží k bezpečnému přenosu souborů mezi počítači přes SSH. Umožňuje uživatelům připojit se k vzdálenému serveru a provádět operace se soubory, jako je nahrávání, stahování a správa souborů.

## Použití
Základní syntaxe příkazu `sftp` je následující:

```bash
sftp [možnosti] [uživatel@hostitel]
```

## Běžné možnosti
- `-P` : Určuje port pro připojení (pokud není standardní).
- `-o` : Umožňuje specifikovat další volby SSH.
- `-v` : Aktivuje podrobné výstupy pro ladění.

## Běžné příklady
1. Připojení k vzdálenému serveru:
   ```bash
   sftp user@hostname
   ```

2. Nahrání souboru na server:
   ```bash
   put localfile.txt
   ```

3. Stáhnout soubor ze serveru:
   ```bash
   get remotefile.txt
   ```

4. Zobrazení seznamu souborů na serveru:
   ```bash
   ls
   ```

5. Vytvoření adresáře na serveru:
   ```bash
   mkdir new_directory
   ```

## Tipy
- Před přenosem souborů se ujistěte, že máte správná oprávnění na serveru.
- Používejte `-v` pro ladění, pokud se vyskytnou problémy s připojením.
- Vytvářejte skripty pro automatizaci opakovaných úloh s `sftp`.