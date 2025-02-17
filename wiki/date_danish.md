# [Linux] Bash date brug: Hent systemets dato og tid

## Overview
`date`-kommandoen bruges til at vise og ændre systemets dato og tid. Den kan også formatere datoer og tider i forskellige formater, hvilket gør den nyttig til scripting og automatisering.

## Usage
Den grundlæggende syntaks for `date`-kommandoen er:

```bash
date [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `date`-kommandoen:

- `+FORMAT`: Angiver et brugerdefineret format for output.
- `-u`: Viser dato og tid i UTC (Coordinated Universal Time).
- `-d STRING`: Angiver en dato ved hjælp af en given streng.
- `-s STRING`: Sætter systemets dato og tid til den angivne streng.

## Common Examples
Her er nogle praktiske eksempler på brugen af `date`-kommandoen:

1. **Vis den aktuelle dato og tid**:
   ```bash
   date
   ```

2. **Vis datoen i et specifikt format**:
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. **Vis datoen i UTC**:
   ```bash
   date -u
   ```

4. **Vis en specifik dato**:
   ```bash
   date -d "2023-10-01"
   ```

5. **Sæt systemets dato og tid** (kræver root-rettigheder):
   ```bash
   sudo date -s "2023-10-01 12:00:00"
   ```

## Tips
- Brug `date +%F` for at få datoen i ISO 8601-format (YYYY-MM-DD), hvilket er nyttigt til databaser.
- Du kan kombinere formateringskoder for at tilpasse output, f.eks. `date "+%A, %d. %B %Y"` for at vise ugedagen, datoen og måneden.
- Vær opmærksom på, at ændring af systemets dato og tid kan påvirke kørende processer og logfiler, så det bør gøres med forsigtighed.