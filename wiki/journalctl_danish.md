# [Linux] Bash journalctl brug: Vise systemlogfiler

## Overview
`journalctl` er et værktøj til at vise og manipulere systemlogfiler, der er gemt af systemd's journal. Det giver brugerne mulighed for at se logbeskeder fra forskellige systemkomponenter og tjenester, hvilket er nyttigt til fejlfinding og overvågning af systemets tilstand.

## Usage
Den grundlæggende syntaks for `journalctl` er som følger:

```bash
journalctl [options] [arguments]
```

## Common Options
- `-b`: Vis logfiler fra den aktuelle opstart.
- `-f`: Følg logfiler i realtid (som `tail -f`).
- `--since`: Vis logfiler fra en bestemt dato og tid.
- `--until`: Vis logfiler indtil en bestemt dato og tid.
- `-u`: Vis logfiler for en specifik systemd-enhed (service).

## Common Examples
Her er nogle praktiske eksempler på, hvordan man bruger `journalctl`:

1. **Vis alle logfiler:**
   ```bash
   journalctl
   ```

2. **Vis logfiler fra den aktuelle opstart:**
   ```bash
   journalctl -b
   ```

3. **Følg logfiler i realtid:**
   ```bash
   journalctl -f
   ```

4. **Vis logfiler fra en specifik enhed (f.eks. sshd):**
   ```bash
   journalctl -u sshd
   ```

5. **Vis logfiler fra en bestemt dato:**
   ```bash
   journalctl --since "2023-10-01" --until "2023-10-05"
   ```

## Tips
- Brug `-p` optionen til at filtrere logfiler efter prioritet (f.eks. `-p err` for fejl).
- Kombiner `--since` og `--until` for at indsnævre tidsrammen for logfilerne.
- Overvej at bruge `grep` sammen med `journalctl` for at finde specifikke logbeskeder, f.eks. `journalctl | grep "error"`.