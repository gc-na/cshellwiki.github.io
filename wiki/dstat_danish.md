# [Linux] Bash dstat brug: Overvåg systemressourcer i realtid

## Overview
dstat er et kraftfuldt værktøj til overvågning af systemressourcer i realtid. Det kombinerer funktionaliteten af flere værktøjer som vmstat, iostat, netstat og ifstat, hvilket gør det muligt at få et omfattende overblik over systemets ydeevne.

## Usage
Den grundlæggende syntaks for dstat er:

```bash
dstat [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for dstat:

- `-c`: Vis CPU-brug.
- `-d`: Vis diskaktivitet.
- `-n`: Vis netværksaktivitet.
- `-r`: Vis hukommelsesbrug.
- `-t`: Vis tidsstempel.
- `--help`: Vis hjælp og tilgængelige muligheder.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du kan bruge dstat:

1. **Vis CPU- og hukommelsesbrug:**
   ```bash
   dstat -c -r
   ```

2. **Vis disk- og netværksaktivitet:**
   ```bash
   dstat -d -n
   ```

3. **Vis alle ressourcer med tidsstempel:**
   ```bash
   dstat -t -c -d -n -r
   ```

4. **Gem output til en fil:**
   ```bash
   dstat > output.txt
   ```

## Tips
- Brug `dstat --help` for at få en liste over alle tilgængelige muligheder og deres forklaringer.
- Kombiner forskellige muligheder for at få et mere detaljeret billede af systemets ydeevne.
- Overvej at køre dstat med `-p` for at se processer, der bruger mest ressourcer, hvis du har brug for at diagnosticere specifikke problemer.