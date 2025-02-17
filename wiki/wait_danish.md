# [Linux] Bash wait brug: Vent på baggrundsprocesser

## Oversigt
`wait`-kommandoen i Bash bruges til at vente på, at en eller flere baggrundsprocesser afslutter. Det er nyttigt, når du ønsker at sikre, at en proces er færdig, før du fortsætter med næste kommando.

## Brug
Den grundlæggende syntaks for `wait`-kommandoen er:

```bash
wait [options] [arguments]
```

## Almindelige muligheder
- `PID`: Angiv en specifik proces-ID at vente på. Hvis ingen PID er angivet, venter `wait` på alle baggrundsprocesser.
- `-n`: Vent på den næste afsluttede baggrundsproces.

## Almindelige eksempler

1. **Vent på alle baggrundsprocesser:**
   ```bash
   sleep 5 &
   sleep 3 &
   wait
   echo "Alle baggrundsprocesser er færdige."
   ```

2. **Vent på en specifik proces:**
   ```bash
   sleep 5 &
   PID=$!
   echo "Venter på proces med PID $PID..."
   wait $PID
   echo "Processen er færdig."
   ```

3. **Vent på den næste afsluttede baggrundsproces:**
   ```bash
   sleep 5 &
   sleep 3 &
   wait -n
   echo "En baggrundsproces er færdig."
   ```

## Tips
- Brug `wait` i scripts for at sikre, at alle nødvendige processer er afsluttet, før scriptet fortsætter.
- Hold øje med proces-ID'er (PID), når du starter baggrundsprocesser, så du kan vente på dem specifikt.
- `wait` kan være nyttig i kombination med andre kommandoer i et script for at synkronisere opgaver.