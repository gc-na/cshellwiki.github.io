# [Linux] Bash usermod použití: Správa uživatelských účtů

## Přehled
Příkaz `usermod` se používá k úpravě existujících uživatelských účtů v systému Linux. Umožňuje administrátorům měnit různé atributy uživatelského účtu, jako jsou skupiny, domovské adresáře a další vlastnosti.

## Použití
Základní syntaxe příkazu `usermod` je následující:

```bash
usermod [možnosti] [uživatelské_jméno]
```

## Běžné možnosti
- `-aG`: Přidá uživatele do specifikovaných skupin, aniž by odebral existující členství.
- `-d`: Změní domovský adresář uživatele.
- `-l`: Změní uživatelské jméno.
- `-s`: Změní výchozí shell uživatele.
- `-g`: Změní primární skupinu uživatele.

## Běžné příklady
1. **Přidání uživatele do skupiny**:
   Přidání uživatele `jan` do skupiny `developers`:
   ```bash
   usermod -aG developers jan
   ```

2. **Změna domovského adresáře**:
   Změna domovského adresáře uživatele `petr` na `/home/petr_new`:
   ```bash
   usermod -d /home/petr_new petr
   ```

3. **Změna uživatelského jména**:
   Změna uživatelského jména z `oldname` na `newname`:
   ```bash
   usermod -l newname oldname
   ```

4. **Změna výchozího shellu**:
   Nastavení výchozího shellu uživatele `anna` na `/bin/zsh`:
   ```bash
   usermod -s /bin/zsh anna
   ```

## Tipy
- Před provedením změn doporučujeme zálohovat důležité údaje uživatele.
- Vždy používejte `-aG` při přidávání uživatelů do skupin, abyste neztratili existující členství.
- Změny provedené pomocí `usermod` mohou vyžadovat odhlášení a přihlášení uživatele, aby se projevily.