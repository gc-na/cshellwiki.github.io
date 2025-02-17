# [Linux] Bash cal brug: Vis kalender

## Oversigt
`cal`-kommandoen bruges til at vise en kalender i terminalen. Den kan vise den aktuelle måned, en specifik måned eller en hel årskalender. Det er en enkel og nyttig måde at få et hurtigt overblik over datoer.

## Brug
Den grundlæggende syntaks for `cal`-kommandoen er:

```bash
cal [options] [arguments]
```

## Almindelige muligheder
- `-m`: Vis kalenderen med den nuværende måned i fokus.
- `-y`: Vis kalenderen for det aktuelle år.
- `-3`: Vis kalenderen for den aktuelle måned samt måneden før og efter.
- `-j`: Vis kalenderen med julian datoer.
- `-A [num]`: Vis de næste [num] måneder.
- `-B [num]`: Vis de forrige [num] måneder.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `cal`:

1. **Vis den nuværende måned**:
   ```bash
   cal
   ```

2. **Vis kalenderen for en specifik måned og år (f.eks. januar 2023)**:
   ```bash
   cal 01 2023
   ```

3. **Vis kalenderen for det aktuelle år**:
   ```bash
   cal -y
   ```

4. **Vis kalenderen for den nuværende måned samt måneden før og efter**:
   ```bash
   cal -3
   ```

5. **Vis kalenderen med julian datoer**:
   ```bash
   cal -j
   ```

## Tips
- Du kan kombinere muligheder for at tilpasse visningen af kalenderen. For eksempel, `cal -3 -A 2` viser den nuværende måned samt de to næste måneder.
- Brug `man cal` for at få mere detaljeret information om kommandoen og dens muligheder.
- Hvis du ofte skal tjekke datoer, kan du overveje at oprette en alias i din `.bashrc`-fil for hurtigere adgang.