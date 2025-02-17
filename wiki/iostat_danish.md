# [Linux] Bash iostat brug: Overvågning af systemets I/O-ydelse

## Oversigt
`iostat`-kommandoen bruges til at overvåge systemets input/output (I/O) ydeevne. Den giver information om CPU-brug og I/O-statistik for enheder og partitioner, hvilket hjælper med at identificere flaskehalse og optimere systemets ydeevne.

## Brug
Den grundlæggende syntaks for `iostat`-kommandoen er:

```bash
iostat [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c`: Viser CPU-statistik.
- `-d`: Viser I/O-statistik for enheder.
- `-x`: Viser udvidede I/O-statistikker.
- `-m`: Viser resultater i megabyte pr. sekund.
- `-t`: Viser tidsstempel for hver rapport.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `iostat` kan bruges:

1. **Vis CPU- og I/O-statistik:**
   ```bash
   iostat
   ```

2. **Vis kun I/O-statistik for enheder:**
   ```bash
   iostat -d
   ```

3. **Vis udvidede I/O-statistikker:**
   ```bash
   iostat -x
   ```

4. **Vis resultater i megabyte pr. sekund:**
   ```bash
   iostat -m
   ```

5. **Vis statistik med tidsstempel:**
   ```bash
   iostat -t
   ```

## Tips
- Brug `iostat` sammen med `-x` for at få en dybere indsigt i I/O-ydelsen, især hvis du har brug for at analysere flaskehalse.
- Overvej at køre `iostat` med en intervalparameter for at overvåge ydeevnen over tid, f.eks. `iostat 5` for at opdatere hver 5. sekund.
- Kombiner `iostat` med andre værktøjer som `top` eller `vmstat` for en mere omfattende systemovervågning.