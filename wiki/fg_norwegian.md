# [Linux] Bash fg Bruk: Gjenoppta en bakgrunnsprosess

## Oversikt
`fg`-kommandoen brukes i Bash for å bringe en bakgrunnsprosess tilbake til forgrunnen. Dette er nyttig når du har startet en prosess i bakgrunnen og ønsker å interagere med den igjen.

## Bruk
Grunnleggende syntaks for `fg`-kommandoen er som følger:

```bash
fg [job_id]
```

## Vanlige alternativer
- `job_id`: Identifikatoren for prosessen du ønsker å bringe til forgrunnen. Hvis du ikke spesifiserer en `job_id`, vil `fg` bringe den siste bakgrunnsprosessen til forgrunnen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `fg`:

1. **Bring den siste bakgrunnsprosessen til forgrunnen:**
   ```bash
   fg
   ```

2. **Bring en spesifikk bakgrunnsprosess til forgrunnen:**
   Først, sjekk bakgrunnsprosessene med `jobs`:
   ```bash
   jobs
   ```
   Deretter, hvis du ser en prosess med job_id 1, kan du bruke:
   ```bash
   fg %1
   ```

3. **Bringe en prosess til forgrunnen etter å ha stoppet den:**
   Hvis du har stoppet en prosess med `Ctrl + Z`, kan du bringe den tilbake med:
   ```bash
   fg
   ```

## Tips
- Hvis du har flere bakgrunnsprosesser, kan du bruke `jobs`-kommandoen for å se dem og deretter bruke `fg %job_id` for å spesifisere hvilken prosess du vil bringe til forgrunnen.
- Husk at når du bringer en prosess til forgrunnen, kan du interagere med den som vanlig, og den vil ta over terminalen til den er fullført eller stoppet.
- Du kan bruke `Ctrl + Z` for å stoppe en prosess og sende den til bakgrunnen, og deretter bruke `fg` for å gjenoppta den når du er klar.