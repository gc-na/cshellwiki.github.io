# [Linux] Bash free kommando: Vis hukommelsesbrug

## Oversigt
Kommandoen `free` bruges til at vise information om systemets hukommelsesbrug, herunder den samlede, brugte og ledige hukommelse. Det er et nyttigt værktøj til at overvåge systemets ydeevne og hukommelsesforbrug.

## Brug
Den grundlæggende syntaks for `free`-kommandoen er som følger:

```bash
free [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h`: Viser hukommelsesoplysninger i et menneskeligt læsbart format (f.eks. MB eller GB).
- `-m`: Viser hukommelsesoplysninger i megabyte.
- `-g`: Viser hukommelsesoplysninger i gigabyte.
- `-s [sekunder]`: Opdaterer visningen med det angivne interval i sekunder.
- `-t`: Viser den samlede hukommelse, inklusive swap.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `free`-kommandoen:

1. **Vis hukommelsesbrug i standardformat:**
   ```bash
   free
   ```

2. **Vis hukommelsesbrug i et menneskeligt læsbart format:**
   ```bash
   free -h
   ```

3. **Vis hukommelsesbrug i megabyte:**
   ```bash
   free -m
   ```

4. **Vis hukommelsesbrug i gigabyte:**
   ```bash
   free -g
   ```

5. **Opdater visningen hvert 5. sekund:**
   ```bash
   free -s 5
   ```

6. **Vis total hukommelse inklusive swap:**
   ```bash
   free -t
   ```

## Tips
- Brug `-h` for at gøre output mere læsbart, især hvis du arbejder med store mængder hukommelse.
- Kombiner `free` med andre kommandoer som `watch` for at overvåge hukommelsesforbruget i realtid:
  ```bash
  watch free -h
  ```
- Tjek hukommelsesforbruget regelmæssigt for at identificere potentielle flaskehalse i systemets ydeevne.