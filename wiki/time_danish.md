# [Linux] Bash time brug: Mål kommandotid

## Oversigt
`time`-kommandoen bruges til at måle den tid, det tager at udføre en given kommando. Den giver oplysninger om den samlede tid, der er brugt på at køre kommandoen, samt detaljer om CPU-tid og systemtid.

## Brug
Den grundlæggende syntaks for `time`-kommandoen er:

```bash
time [options] [arguments]
```

## Almindelige muligheder
- `-p`: Udskriver tiden i POSIX-format.
- `-o <fil>`: Gemmer output i den angivne fil.
- `-v`: Viser detaljeret information om ressourcer, der er brugt af kommandoen.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `time`-kommandoen:

1. Mål tiden for at køre et script:
   ```bash
   time ./mit_script.sh
   ```

2. Mål tiden for at køre en kommando og gem output til en fil:
   ```bash
   time -o output.txt ls -l
   ```

3. Få detaljeret information om ressourcer brugt af en kommando:
   ```bash
   time -v sleep 2
   ```

## Tips
- Brug `-p` for at få et mere læsbart output, der er nemt at sammenligne.
- Overvej at gemme output til en fil, hvis du vil analysere resultaterne senere.
- `time` kan bruges med enhver kommando, så du kan måle ydeevnen af forskellige scripts og programmer.