# [Linux] Bash ved at: Planlæg opgaver til fremtiden

## Oversigt
`at`-kommandoen bruges til at planlægge opgaver, der skal udføres på et bestemt tidspunkt i fremtiden. Det er en praktisk måde at automatisere opgaver, der skal køre én gang.

## Brug
Den grundlæggende syntaks for `at`-kommandoen er:

```bash
at [options] [arguments]
```

## Almindelige muligheder
- `-f FILE`: Angiver en fil, der indeholder de kommandoer, der skal køres.
- `-m`: Sender en e-mail, hvis jobben mislykkes.
- `-q QUEUE`: Angiver en specifik kø, hvor jobben skal placeres.
- `-l`: Viser en liste over planlagte job.
- `-d JOB_ID`: Sletter et planlagt job.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `at`:

1. **Planlæg en opgave til at køre nu**:
   ```bash
   echo "echo 'Hello, World!'" | at now
   ```

2. **Planlæg en opgave til at køre i morgen kl. 10:00**:
   ```bash
   echo "backup.sh" | at 10:00 tomorrow
   ```

3. **Planlæg en opgave fra en fil**:
   ```bash
   at -f /path/to/script.sh 14:00
   ```

4. **Vis alle planlagte opgaver**:
   ```bash
   at -l
   ```

5. **Slet et planlagt job**:
   ```bash
   at -d 5
   ```

## Tips
- Sørg for, at `atd`-daemonen kører, ellers vil dine planlagte opgaver ikke blive udført.
- Brug `at -l` regelmæssigt for at holde styr på dine planlagte opgaver.
- Tænk over, hvornår du planlægger opgaver, så de ikke overlapper med andre vigtige processer.