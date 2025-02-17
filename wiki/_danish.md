# [Linux] Bash @ brug: Udfør kommandoer i baggrunden

## Oversigt
Kommandoen `@` i Bash bruges til at køre en given kommando i baggrunden, så du kan fortsætte med at bruge terminalen til andre opgaver, mens den kører.

## Brug
Den grundlæggende syntaks for `@` kommandoen er:
```bash
@ [options] [arguments]
```

## Almindelige muligheder
- `&` - Kører kommandoen i baggrunden.
- `disown` - Fjerner en baggrundsjob fra joblisten, så det ikke længere er knyttet til terminalen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `@` kommandoen:

1. Kør en scriptfil i baggrunden:
   ```bash
   ./mit_script.sh &
   ```

2. Kør en langvarig opgave i baggrunden:
   ```bash
   sleep 100 &
   ```

3. Kør en kommando og fjern den fra joblisten:
   ```bash
   long_running_command &
   disown
   ```

## Tips
- Brug `jobs` for at se en liste over aktive baggrundsjob.
- For at bringe et baggrundsjob tilbage til forgrunden, kan du bruge `fg %jobnummer`.
- Vær opmærksom på, at hvis du lukker terminalen, kan baggrundsjob blive afsluttet, medmindre du bruger `disown`.