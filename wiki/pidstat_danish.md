# [Linux] Bash pidstat Brug: Overvågning af processtatistik

## Overview
`pidstat` er et værktøj, der bruges til at overvåge og rapportere statistik om kørende processer i Linux. Det giver detaljerede oplysninger om CPU-brug, hukommelsesforbrug og andre ressourcer, der anvendes af specifikke processer.

## Usage
Den grundlæggende syntaks for `pidstat` er som følger:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Viser hjælp og tilgængelige muligheder.
- `-p <pid>`: Angiver den specifikke proces-ID (PID) for den proces, der skal overvåges.
- `-r`: Viser hukommelsesbrug for processer.
- `-u`: Viser CPU-brug for processer.
- `-t`: Viser statistik for tråde i stedet for processer.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du kan bruge `pidstat`:

1. **Vis CPU-brug for alle processer:**
   ```bash
   pidstat -u
   ```

2. **Vis hukommelsesbrug for en specifik proces (PID 1234):**
   ```bash
   pidstat -r -p 1234
   ```

3. **Overvåg CPU- og hukommelsesbrug for alle processer hver 2. sekund:**
   ```bash
   pidstat -u -r 2
   ```

4. **Vis trådstatistik for en specifik proces (PID 5678):**
   ```bash
   pidstat -t -p 5678
   ```

## Tips
- Brug `pidstat` sammen med `watch` for at opdatere visningen i realtid:
  ```bash
  watch -n 1 pidstat -u
  ```
- Kombiner `pidstat` med andre værktøjer som `grep` for at filtrere specifikke processer.
- Tjek `man pidstat` for at få en dybere forståelse af alle tilgængelige muligheder og deres anvendelser.