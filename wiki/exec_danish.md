# [Linux] Bash exec brug: Kør et kommando i den nuværende shell

## Oversigt
`exec`-kommandoen bruges i Bash til at erstatte den aktuelle shell-proces med en ny kommando. Dette betyder, at når du bruger `exec`, vil den nuværende shell ikke længere eksistere, og den vil blive erstattet af den angivne kommando.

## Brug
Den grundlæggende syntaks for `exec`-kommandoen er:

```bash
exec [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a` : Angiv et alternativt navn til den kørende proces.
- `-l` : Start den nye shell som en login-shell.
- `-c` : Kør kommandoen i en ny shell.

## Almindelige eksempler

1. **Erstat den nuværende shell med en ny kommando:**
   ```bash
   exec ls -l
   ```
   Dette vil liste indholdet af den nuværende mappe og erstatte den nuværende shell med `ls`-kommandoen.

2. **Kør en shell som en login-shell:**
   ```bash
   exec -l bash
   ```
   Dette vil starte en ny Bash-shell som en login-shell.

3. **Angiv et alternativt navn til processen:**
   ```bash
   exec -a mit_navn /bin/bash
   ```
   Dette vil starte en ny Bash-shell, men den vil blive vist som `mit_navn` i proceslisten.

## Tips
- Vær opmærksom på, at når du bruger `exec`, vil den nuværende shell blive afsluttet, så sørg for at gemme eventuelle nødvendige data før du kører kommandoen.
- `exec` er nyttigt i scripts, hvor du ønsker at erstatte den nuværende proces med en anden kommando uden at starte en ny shell.
- Brug `exec` i kombination med redirection for at omdirigere output til filer eller andre processer.