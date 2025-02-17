# [Linux] Bash journalctl användning: Visa systemloggar

## Översikt
`journalctl` är ett kommando som används för att visa loggar som samlas in av systemd-journald. Det ger en enkel och effektiv metod för att granska system- och tjänstloggar, vilket hjälper administratörer att felsöka problem och övervaka systemets hälsa.

## Användning
Den grundläggande syntaxen för `journalctl` ser ut som följer:

```bash
journalctl [alternativ] [argument]
```

## Vanliga alternativ
- `-b` : Visa loggar från den senaste systemstarten.
- `-f` : Följ loggar i realtid (liknande `tail -f`).
- `--since` : Visa loggar från ett specifikt datum och tid.
- `--until` : Visa loggar fram till ett specifikt datum och tid.
- `-u <tjänst>` : Visa loggar för en specifik systemtjänst.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `journalctl`:

1. Visa alla loggar:
   ```bash
   journalctl
   ```

2. Visa loggar från den senaste systemstarten:
   ```bash
   journalctl -b
   ```

3. Följ loggar i realtid:
   ```bash
   journalctl -f
   ```

4. Visa loggar för en specifik tjänst, till exempel `ssh.service`:
   ```bash
   journalctl -u ssh.service
   ```

5. Visa loggar från en specifik tidpunkt:
   ```bash
   journalctl --since "2023-10-01 10:00:00" --until "2023-10-01 12:00:00"
   ```

## Tips
- Använd `-p <prioritet>` för att filtrera loggar efter prioritet, till exempel `-p err` för att visa endast felmeddelanden.
- Kombinera alternativ för att få mer specifika resultat, som att följa loggar för en tjänst: `journalctl -u ssh.service -f`.
- Tänk på att loggar kan vara stora, så använd `--no-pager` om du vill se allt i en gång utan att paginera.