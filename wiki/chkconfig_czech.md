# [Linux] Bash chkconfig použití: Správa systémových služeb

## Přehled
Příkaz `chkconfig` slouží k správě systémových služeb v Linuxu, zejména pro konfiguraci, které služby se mají spouštět při startu systému. Umožňuje uživatelům snadno zapínat nebo vypínat služby pro různé úrovně spuštění.

## Použití
Základní syntaxe příkazu je následující:

```bash
chkconfig [možnosti] [argumenty]
```

## Běžné možnosti
- `--list`: Zobrazí seznam všech služeb a jejich stav pro jednotlivé úrovně spuštění.
- `--add`: Přidá novou službu do správy chkconfig.
- `--del`: Odebere službu ze správy chkconfig.
- `--level`: Určuje úrovně spuštění, pro které se mají provést akce (např. 2345).
- `on`: Aktivuje službu pro zvolenou úroveň spuštění.
- `off`: Deaktivuje službu pro zvolenou úroveň spuštění.

## Běžné příklady
- Zobrazení stavu všech služeb:
```bash
chkconfig --list
```

- Aktivace služby `httpd` pro úrovně spuštění 2, 3 a 5:
```bash
chkconfig --level 235 httpd on
```

- Deaktivace služby `ftp` pro všechny úrovně spuštění:
```bash
chkconfig ftp off
```

- Přidání nové služby `myservice`:
```bash
chkconfig --add myservice
```

- Odebrání služby `myservice`:
```bash
chkconfig --del myservice
```

## Tipy
- Před provedením změn v konfiguraci služeb je dobré si zkontrolovat aktuální stav pomocí `chkconfig --list`.
- Ujistěte se, že máte potřebná oprávnění (např. spouštět příkazy jako root), abyste mohli měnit konfiguraci služeb.
- Po provedení změn je doporučeno restartovat systém, aby se změny projevily.