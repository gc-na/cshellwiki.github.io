# [Linux] Bash vipw použití: Upravuje soubor s uživatelskými účty

## Přehled
Příkaz `vipw` slouží k bezpečné úpravě souboru s uživatelskými účty, obvykle `/etc/passwd` a `/etc/shadow`. Tento příkaz zajišťuje, že během úprav nedojde k žádným konfliktům, což je důležité pro zachování integrity systému.

## Použití
Základní syntaxe příkazu je následující:

```bash
vipw [options]
```

## Běžné možnosti
- `-s`: Upravuje soubor `/etc/shadow` místo `/etc/passwd`.
- `-h`: Zobrazí pomoc s příkazem.

## Běžné příklady
1. **Úprava souboru s uživatelskými účty:**
   ```bash
   vipw
   ```

2. **Úprava souboru s hesly uživatelů:**
   ```bash
   vipw -s
   ```

3. **Zobrazení nápovědy k příkazu:**
   ```bash
   vipw -h
   ```

## Tipy
- Před použitím příkazu `vipw` se ujistěte, že máte potřebná oprávnění, obvykle jako uživatel root.
- Vždy zálohujte soubory `/etc/passwd` a `/etc/shadow` před jejich úpravou, abyste se vyhnuli ztrátě dat.
- Používejte `vipw` místo běžného textového editoru pro úpravy těchto souborů, aby se minimalizovalo riziko poškození systému.