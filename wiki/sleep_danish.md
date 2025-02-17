# [Linux] Bash sleep brug: Pauser udførelsen af et script i et bestemt tidsrum

## Oversigt
`sleep`-kommandoen bruges til at pause udførelsen af et script eller en kommando i et angivet tidsrum. Det er nyttigt, når du ønsker at indføre forsinkelser mellem kommandoer eller i scripts.

## Brug
Den grundlæggende syntaks for `sleep`-kommandoen er som følger:

```bash
sleep [options] [arguments]
```

## Almindelige muligheder
- `-s`, `--seconds`: Angiver tidsrummet i sekunder (standard).
- `-m`, `--minutes`: Angiver tidsrummet i minutter.
- `-h`, `--hours`: Angiver tidsrummet i timer.
- `-d`, `--days`: Angiver tidsrummet i dage.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `sleep`:

1. Pause i 5 sekunder:
   ```bash
   sleep 5
   ```

2. Pause i 2 minutter:
   ```bash
   sleep 2m
   ```

3. Pause i 1 time:
   ```bash
   sleep 1h
   ```

4. Pause i 3 dage:
   ```bash
   sleep 3d
   ```

5. Brug `sleep` i et script til at vente mellem kommandoer:
   ```bash
   echo "Starter op..."
   sleep 10
   echo "Fortsætter efter 10 sekunder."
   ```

## Tips
- Brug `sleep` til at undgå overbelastning af systemressourcer ved at indføre pauser mellem gentagne kommandoer.
- Kombiner `sleep` med `&&` for at sikre, at den næste kommando kun køres efter pausen.
- Vær opmærksom på, at `sleep` accepterer decimaler, så du kan pause i f.eks. 1,5 sekunder ved at skrive `sleep 1.5`.