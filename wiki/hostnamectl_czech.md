# [Linux] Bash hostnamectl použití: Správa názvu hostitele a dalších informací o systému

## Přehled
Příkaz `hostnamectl` slouží k zobrazení a správě názvu hostitele systému, stejně jako dalších informací o systému, jako je operační systém, architektura a verze jádra.

## Použití
Základní syntaxe příkazu je následující:

```bash
hostnamectl [možnosti] [argumenty]
```

## Běžné možnosti
- `set-hostname`: Nastaví nový název hostitele.
- `status`: Zobrazí aktuální informace o systému a názvu hostitele.
- `set-chassis`: Nastaví typ šasi (např. desktop, server).
- `set-icon-name`: Nastaví ikonu systému podle názvu hostitele.

## Běžné příklady
Několik praktických příkladů použití příkazu `hostnamectl`:

1. Zobrazení aktuálního názvu hostitele a informací o systému:
   ```bash
   hostnamectl status
   ```

2. Nastavení nového názvu hostitele:
   ```bash
   sudo hostnamectl set-hostname novy-nazev
   ```

3. Nastavení typu šasi na server:
   ```bash
   sudo hostnamectl set-chassis server
   ```

4. Nastavení ikony systému:
   ```bash
   sudo hostnamectl set-icon-name server
   ```

## Tipy
- Při změně názvu hostitele je dobré restartovat systém, aby se změna projevila.
- Používejte jasné a popisné názvy hostitelů, aby bylo snadné identifikovat zařízení v síti.
- Zkontrolujte, zda máte potřebná oprávnění (např. administrátorská práva) pro provádění změn pomocí `hostnamectl`.