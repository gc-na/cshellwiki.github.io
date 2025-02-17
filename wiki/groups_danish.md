# [Linux] Bash grupperer brugere: Viser brugergrupper

## Oversigt
`groups`-kommandoen bruges til at vise de grupper, som en bruger tilhører. Det er en nyttig måde at få indsigt i brugerens rettigheder og adgangsniveauer i systemet.

## Brug
Den grundlæggende syntaks for `groups`-kommandoen er:

```bash
groups [options] [arguments]
```

## Almindelige muligheder
- `-h`, `--help`: Viser en hjælpemeddelelse med information om brugen af kommandoen.
- `-n`, `--no-group`: Viser kun brugerens grupper uden at inkludere gruppenavne.
- `--version`: Viser versionsoplysninger om `groups`-kommandoen.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `groups`-kommandoen:

1. **Vis grupper for den aktuelle bruger:**
   ```bash
   groups
   ```

2. **Vis grupper for en specifik bruger:**
   ```bash
   groups brugernavn
   ```

3. **Vis grupper uden gruppenavne:**
   ```bash
   groups -n brugernavn
   ```

4. **Få hjælp til kommandoen:**
   ```bash
   groups --help
   ```

## Tips
- Brug `groups`-kommandoen regelmæssigt for at sikre, at du har de nødvendige rettigheder til at udføre opgaver på systemet.
- Kombiner `groups` med andre kommandoer som `id` for at få en mere detaljeret oversigt over brugerens identitet og rettigheder.
- Hvis du arbejder med flere brugere, kan det være nyttigt at lave scripts, der automatisk kontrollerer gruppetilhørsforhold for at sikre korrekt adgangskontrol.