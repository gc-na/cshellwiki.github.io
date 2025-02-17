# [Linux] Bash vmstat brug: Overvågning af systemets ressourcer

## Overview
`vmstat` (virtual memory statistics) er et værktøj til overvågning af systemets ressourcer, der giver information om hukommelse, processer, ind- og uddata samt CPU-aktivitet. Det hjælper brugere med at forstå systemets ydeevne og identificere flaskehalse.

## Usage
Den grundlæggende syntaks for `vmstat` er:

```bash
vmstat [options] [arguments]
```

## Common Options
- `-a`: Viser alle hukommelsesstatistikker, inklusive aktiv og inaktiv hukommelse.
- `-m`: Viser statistik for hukommelsesblokke.
- `-s`: Viser en samlet oversigt over systemets hukommelse og processer.
- `-t`: Viser tidsstempel for hver række af output.
- `delay`: Angiver tidsintervallet (i sekunder) mellem opdateringer af output.

## Common Examples
Her er nogle praktiske eksempler på brugen af `vmstat`:

1. **Vis grundlæggende systemstatistikker**:
   ```bash
   vmstat
   ```

2. **Vis opdateret statistik hvert 5. sekund**:
   ```bash
   vmstat 5
   ```

3. **Vis statistik med tidsstempel**:
   ```bash
   vmstat -t 5
   ```

4. **Vis detaljeret hukommelsesstatistik**:
   ```bash
   vmstat -a
   ```

5. **Vis statistik for hukommelsesblokke**:
   ```bash
   vmstat -m
   ```

## Tips
- Brug `vmstat` sammen med andre værktøjer som `top` eller `htop` for en mere omfattende overvågning af systemets ydeevne.
- Overvåg output over tid for at identificere mønstre i systemets belastning og hukommelsesforbrug.
- Vær opmærksom på, at `vmstat` viser gennemsnitlige værdier; for mere detaljerede analyser kan det være nødvendigt at kombinere det med andre værktøjer.