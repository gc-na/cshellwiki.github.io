# [Linux] Bash jobs brug: Vise baggrundsopgaver

## Oversigt
`jobs`-kommandoen bruges til at vise en liste over baggrundsopgaver, der kører i den aktuelle shell-session. Det giver brugeren mulighed for at se status for disse opgaver, såsom om de kører, er stoppet eller er afsluttet.

## Brug
Den grundlæggende syntaks for `jobs`-kommandoen er:

```bash
jobs [options]
```

## Almindelige muligheder
- `-l`: Viser job-ID'er (PID) sammen med jobbeskrivelserne.
- `-n`: Viser kun jobs, der har ændret status siden den sidste gang `jobs` blev kørt.
- `-p`: Viser kun job-ID'erne for baggrundsopgaverne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `jobs`-kommandoen:

1. **Vis alle baggrundsopgaver:**
   ```bash
   jobs
   ```

2. **Vis baggrundsopgaver med job-ID'er:**
   ```bash
   jobs -l
   ```

3. **Vis kun jobs, der har ændret status:**
   ```bash
   jobs -n
   ```

4. **Vis kun job-ID'er:**
   ```bash
   jobs -p
   ```

## Tips
- Brug `bg`-kommandoen til at genoptage en stoppet opgave i baggrunden.
- Brug `fg`-kommandoen til at bringe en baggrundsopgave tilbage til forgrunden.
- Hold øje med status for dine opgaver, især når du arbejder med flere processer, for at undgå forvirring.