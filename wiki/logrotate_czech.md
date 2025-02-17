# [Linux] Bash logrotate použití: Správa logovacích souborů

## Přehled
Příkaz `logrotate` slouží k automatizaci správy logovacích souborů v systému. Umožňuje pravidelně otáčet, komprimovat a odstraňovat staré logy, což pomáhá udržovat systém přehledný a šetřit místo na disku.

## Použití
Základní syntaxe příkazu `logrotate` je následující:

```bash
logrotate [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`: Vynutí provedení rotace logů, i když to není potřeba.
- `-s`: Určuje soubor pro sledování stavu rotace.
- `-v`: Zobrazí podrobné informace o prováděných akcích.
- `-d`: Spustí logrotate v "suchém" režimu, což znamená, že pouze zobrazí, co by bylo provedeno, ale nic neprovede.

## Běžné příklady
1. **Základní rotace logů podle konfiguračního souboru:**

```bash
logrotate /etc/logrotate.conf
```

2. **Vynucení rotace logů:**

```bash
logrotate -f /etc/logrotate.conf
```

3. **Zobrazení podrobných informací o rotaci:**

```bash
logrotate -v /etc/logrotate.conf
```

4. **Spuštění v "suchém" režimu:**

```bash
logrotate -d /etc/logrotate.conf
```

## Tipy
- Ujistěte se, že máte správně nastavené konfigurační soubory pro logrotate, aby se rotace prováděla podle vašich potřeb.
- Pravidelně kontrolujte logy a výstupy logrotate, abyste se ujistili, že nedochází k problémům s rotací.
- Zvažte nastavení cron úlohy pro pravidelnou rotaci logů, pokud to není již součástí vašeho systému.