# [Linux] Bash journalctl použití: Zobrazování systémových logů

## Přehled
Příkaz `journalctl` slouží k prohlížení a správě logů systému, které jsou uchovávány v systemd journalu. Umožňuje uživatelům přístup k různým záznamům, jako jsou systémové události, chybové hlášení a další diagnostické informace.

## Použití
Základní syntaxe příkazu je následující:
```bash
journalctl [možnosti] [argumenty]
```

## Běžné možnosti
- `-b` nebo `--boot`: Zobrazí logy pouze z aktuálního spuštění systému.
- `-f` nebo `--follow`: Sleduje logy v reálném čase, podobně jako příkaz `tail -f`.
- `-p` nebo `--priority`: Filtruje logy podle priority (např. `-p err` zobrazí pouze chybové zprávy).
- `-u` nebo `--unit`: Zobrazí logy pro konkrétní službu (např. `-u ssh.service`).
- `--since` a `--until`: Umožňují specifikovat časový interval pro zobrazení logů.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `journalctl`:

### Zobrazení všech logů
```bash
journalctl
```

### Zobrazení logů z aktuálního spuštění
```bash
journalctl -b
```

### Sledování logů v reálném čase
```bash
journalctl -f
```

### Zobrazení pouze chybových zpráv
```bash
journalctl -p err
```

### Zobrazení logů pro konkrétní službu
```bash
journalctl -u ssh.service
```

### Zobrazení logů za určité období
```bash
journalctl --since "2023-10-01" --until "2023-10-31"
```

## Tipy
- Používejte kombinaci možností pro efektivnější filtrování logů.
- Pravidelně kontrolujte logy, abyste měli přehled o stavu systému a případných problémech.
- Zvažte použití příkazu `grep` pro další filtrování logů podle klíčových slov.