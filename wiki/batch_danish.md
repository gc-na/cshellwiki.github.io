# [Linux] Bash batch brug: Kør kommandoer i baggrunden

## Oversigt
`batch`-kommandoen bruges til at planlægge opgaver, der skal køres i baggrunden, når systemet har ledige ressourcer. Det er nyttigt til at udføre langvarige opgaver uden at belaste systemet, når det er under høj belastning.

## Brug
Den grundlæggende syntaks for `batch`-kommandoen er:

```bash
batch [options] [arguments]
```

## Almindelige muligheder
- `-f`: Angiv en fil, der indeholder kommandoer, der skal køres.
- `-q`: Kør i stille tilstand, uden at vise output.
- `-l`: Angiv en specifik tidsplan for, hvornår opgaven skal køres.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `batch`-kommandoen:

1. Kør en simpel kommando i baggrunden:
   ```bash
   echo "Hello, World!" | batch
   ```

2. Kør en kommando fra en fil:
   ```bash
   batch < my_commands.txt
   ```

3. Kør en kommando med stille tilstand:
   ```bash
   echo "Backup started" | batch -q
   ```

4. Angiv en specifik tidsplan:
   ```bash
   echo "Run maintenance script" | batch -l "now + 1 hour"
   ```

## Tips
- Sørg for at kontrollere, at systemet har tilstrækkelige ressourcer, før du sender opgaver til `batch`.
- Brug `at`-kommandoen, hvis du har brug for mere præcise tidsplaner.
- Hold dine batch-kommandoer enkle for at undgå fejl under udførelsen.