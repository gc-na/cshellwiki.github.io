# [Linux] Bash bg brug: Sætte job i baggrunden

## Oversigt
`bg`-kommandoen bruges i Bash til at fortsætte et stoppet job i baggrunden. Dette er nyttigt, når du ønsker at frigøre terminalen, mens et program stadig kører.

## Brug
Den grundlæggende syntaks for `bg`-kommandoen er:

```bash
bg [job_id]
```

## Almindelige muligheder
- `job_id`: Identifikatoren for det job, du ønsker at køre i baggrunden. Hvis du ikke angiver et job_id, vil `bg` som standard anvende det seneste stoppede job.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `bg`-kommandoen:

1. **Sætte det seneste stoppede job i baggrunden**:
   ```bash
   bg
   ```

2. **Sætte et specifikt job i baggrunden**:
   Antag, at du har stoppet et job med job_id 1.
   ```bash
   bg %1
   ```

3. **Kombinere med `jobs`-kommandoen**:
   Først kan du liste dine jobs:
   ```bash
   jobs
   ```
   Derefter kan du sætte et af dem i baggrunden:
   ```bash
   bg %2
   ```

## Tips
- Brug `jobs`-kommandoen for at se en liste over alle aktive og stoppede jobs, før du bruger `bg`.
- Du kan kombinere `bg` med `fg` for at skifte mellem baggrunds- og forgrundsjob.
- Husk at bruge `&` i slutningen af en kommando, hvis du ønsker at starte et job direkte i baggrunden fra starten. For eksempel:
  ```bash
  long_running_command &
  ```