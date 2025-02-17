# [Linux] Bash groupmod použití: Správa skupin uživatelů

## Přehled
Příkaz `groupmod` slouží k úpravě existujících skupin v systému Linux. Umožňuje měnit různé atributy skupiny, jako je její název nebo identifikační číslo (GID).

## Použití
Základní syntaxe příkazu `groupmod` je následující:

```bash
groupmod [možnosti] [argumenty]
```

## Běžné možnosti
- `-n, --new-name NOVÝ_NÁZEV`: Změní název skupiny na zadaný nový název.
- `-g, --gid NOVÝ_GID`: Změní GID skupiny na zadané číslo.
- `-o, --non-unique`: Umožňuje použití neunikátního GID (pokud je to potřeba).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `groupmod`:

### Změna názvu skupiny
Pokud chcete změnit název skupiny z `stara_skupina` na `nova_skupina`, použijte:

```bash
groupmod -n nova_skupina stara_skupina
```

### Změna GID skupiny
Chcete-li změnit GID skupiny `moje_skupina` na `1001`, použijte:

```bash
groupmod -g 1001 moje_skupina
```

### Změna názvu a GID současně
Pokud potřebujete změnit jak název, tak GID skupiny, můžete to udělat v jednom příkazu:

```bash
groupmod -n nova_skupina -g 1002 stara_skupina
```

## Tipy
- Před provedením změn se ujistěte, že nemáte aktivní uživatele ve skupině, kterou chcete upravit.
- Vždy zálohujte důležité konfigurační soubory před provedením změn.
- Používejte příkaz `getent group` k ověření aktuálních skupin a jejich atributů před a po provedení změn.