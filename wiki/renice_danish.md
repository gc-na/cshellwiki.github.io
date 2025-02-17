# [Linux] Bash renice brug: Juster prioriteten af kørende processer

## Oversigt
`renice`-kommandoen bruges til at ændre prioriteten af en eller flere kørende processer i Linux. Ved at justere prioriteten kan du styre, hvor meget CPU-tid en proces får i forhold til andre processer.

## Brug
Den grundlæggende syntaks for `renice` er som følger:

```bash
renice [options] [arguments]
```

## Almindelige muligheder
- `-n, --priority <value>`: Angiv den nye prioritet for processen. Værdien kan være mellem -20 (højeste prioritet) og 19 (laveste prioritet).
- `-p, --pid <pid>`: Angiv PID (Process ID) for den proces, hvis prioritet du vil ændre.
- `-g, --pgrp <pgrp>`: Angiv procesgruppen, hvis prioritet du vil ændre.
- `-u, --user <user>`: Angiv brugeren, hvis processer du vil ændre prioritet for.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `renice`:

1. Ændre prioriteten af en proces med PID 1234 til 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Ændre prioriteten for alle processer, der tilhører brugeren "john", til 5:
   ```bash
   renice -n 5 -u john
   ```

3. Ændre prioriteten af en procesgruppe med gruppe-ID 5678 til -5:
   ```bash
   renice -n -5 -g 5678
   ```

4. Tjekke nuværende prioritet for en proces med PID 1234:
   ```bash
   ps -o pid,ni,cmd -p 1234
   ```

## Tips
- Vær forsigtig med at sætte prioriteten for systemprocesser til en højere værdi, da det kan påvirke systemets stabilitet.
- Brug `renice` med administrative rettigheder (f.eks. som root) for at ændre prioriteten af processer, der tilhører andre brugere.
- Overvåg systemets ydeevne efter ændringer for at sikre, at dine justeringer har den ønskede effekt.