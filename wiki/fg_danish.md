# [Linux] Bash fg brug: Bring a background job to the foreground

## Oversigt
`fg`-kommandoen bruges i Bash til at bringe en kørende baggrundsopgave tilbage til forgrunden. Dette er nyttigt, når du ønsker at interagere med en proces, der tidligere er blevet sendt til baggrunden.

## Brug
Den grundlæggende syntaks for `fg`-kommandoen er:

```bash
fg [options] [job_spec]
```

## Almindelige muligheder
- `job_spec`: Angiver hvilken opgave der skal bringes til forgrunden. Dette kan være et jobnummer eller en job-ID.
- `-n`: Bring den nyeste baggrundsopgave til forgrunden.

## Almindelige eksempler

1. **Bring den seneste baggrundsopgave til forgrunden:**
   ```bash
   fg
   ```

2. **Bring en specifik baggrundsopgave til forgrunden ved hjælp af jobnummer:**
   ```bash
   fg %1
   ```

3. **Bring en baggrundsopgave til forgrunden ved hjælp af job-ID:**
   ```bash
   fg %2
   ```

4. **Bring den nyeste baggrundsopgave til forgrunden med -n mulighed:**
   ```bash
   fg -n
   ```

## Tips
- Brug `jobs`-kommandoen for at se en liste over kørende baggrundsopgaver og deres jobnumre.
- Hvis du har flere baggrundsopgaver, kan du angive det specifikke jobnummer for at undgå forvirring.
- Husk, at når en opgave er bragt til forgrunden, kan du interagere med den, som du ville gøre med enhver anden proces.