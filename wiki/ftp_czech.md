# [Linux] Bash ftp použití: Přenos souborů mezi počítači

## Přehled
Příkaz `ftp` (File Transfer Protocol) slouží k přenosu souborů mezi počítači přes síť. Umožňuje uživatelům připojit se k FTP serverům a provádět různé operace se soubory, jako je nahrávání, stahování a správa souborů.

## Použití
Základní syntaxe příkazu `ftp` je následující:

```
ftp [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Vypne interaktivní režim, což znamená, že se nebudou ptát na potvrzení při přenosu souborů.
- `-n`: Zabrání automatickému přihlášení k FTP serveru.
- `-v`: Zapne podrobný výstup, což je užitečné pro ladění.
- `-p`: Používá pasivní režim pro připojení, což může být užitečné za určitých síťových podmínek.

## Běžné příklady
### Připojení k FTP serveru
```bash
ftp ftp.example.com
```

### Přihlášení s uživatelským jménem
```bash
ftp -n ftp.example.com
user username password
```

### Nahrání souboru na server
```bash
put soubor.txt
```

### Stažení souboru ze serveru
```bash
get soubor.txt
```

### Zobrazení seznamu souborů na serveru
```bash
ls
```

### Odhlášení z FTP serveru
```bash
bye
```

## Tipy
- Při přenosu citlivých dat zvažte použití `sftp`, což je bezpečnější varianta FTP.
- Vždy se ujistěte, že máte správná oprávnění pro přístup k souborům na serveru.
- Používejte pasivní režim (`-p`), pokud máte problémy s připojením za firewallem.