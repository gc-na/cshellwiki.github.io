# [Linux] Bash e2fsck použití: Oprava souborových systémů

## Přehled
Příkaz `e2fsck` slouží k kontrole a opravě souborových systémů založených na ext2, ext3 a ext4. Je to důležitý nástroj pro údržbu a zajištění integrity dat na těchto typech souborových systémů.

## Použití
Základní syntaxe příkazu `e2fsck` je následující:

```
e2fsck [možnosti] [argumenty]
```

## Běžné možnosti
- `-p`: Automaticky opraví chyby bez interakce uživatele.
- `-f`: Vynutí kontrolu souborového systému, i když se zdá být v pořádku.
- `-n`: Provede kontrolu bez oprav, což je užitečné pro diagnostiku.
- `-y`: Odpoví "ano" na všechny otázky, což znamená, že všechny opravy budou provedeny automaticky.

## Běžné příklady
1. Kontrola souborového systému na zařízení `/dev/sda1`:
   ```bash
   e2fsck /dev/sda1
   ```

2. Automatická oprava chyb bez interakce:
   ```bash
   e2fsck -p /dev/sda1
   ```

3. Vynucení kontroly souborového systému:
   ```bash
   e2fsck -f /dev/sda1
   ```

4. Kontrola bez oprav pro diagnostiku:
   ```bash
   e2fsck -n /dev/sda1
   ```

5. Automatické opravy se souhlasem na všechny otázky:
   ```bash
   e2fsck -y /dev/sda1
   ```

## Tipy
- Před použitím `e2fsck` se ujistěte, že je souborový systém odpojený, aby se předešlo poškození dat.
- Pravidelně kontrolujte souborové systémy, zejména po nečekaných vypnutích nebo pádech systému.
- Vytvářejte zálohy důležitých dat před prováděním oprav, abyste minimalizovali riziko ztráty dat.