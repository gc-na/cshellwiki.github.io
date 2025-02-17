# [Linux] Bash mpstat Brug: Overvågning af CPU-ydelse

## Oversigt
`mpstat` er et værktøj, der bruges til at overvåge CPU-ydelse på et system. Det giver information om CPU-brug pr. processor, hvilket hjælper med at identificere flaskehalse og optimere systemets ydeevne.

## Brug
Den grundlæggende syntaks for `mpstat`-kommandoen er som følger:

```bash
mpstat [options] [arguments]
```

## Almindelige muligheder
- `-P ALL`: Viser statistik for alle CPU'er.
- `-u`: Viser CPU-brug i procent.
- `-h`: Viser output i et mere læsbart format.
- `interval`: Angiver, hvor ofte (i sekunder) data skal opdateres.
- `count`: Angiver, hvor mange gange data skal opdateres.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `mpstat`:

1. **Vis CPU-brug for alle CPU'er:**
   ```bash
   mpstat -P ALL
   ```

2. **Vis CPU-brug med opdatering hvert 2. sekund:**
   ```bash
   mpstat 2
   ```

3. **Vis CPU-brug for en specifik CPU (f.eks. CPU 0):**
   ```bash
   mpstat -P 0
   ```

4. **Vis CPU-statistik i et mere læsbart format:**
   ```bash
   mpstat -h
   ```

## Tips
- Brug `mpstat -P ALL` for at få et overblik over alle CPU'ers ydeevne, især på systemer med flere kerner.
- Overvåg CPU-brug over tid ved at angive både `interval` og `count` for at se tendenser.
- Kombiner `mpstat` med andre værktøjer som `grep` for at filtrere specifik information, hvis du kun er interesseret i bestemte data.