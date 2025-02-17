# [Linux] Bash nice brug: Juster processprioritet

## Overview
`nice`-kommandoen bruges til at ændre prioriteten af en kørende proces i Linux. Det giver brugeren mulighed for at angive, hvor "venlig" en proces skal være over for systemressourcerne, hvilket kan hjælpe med at forbedre systemets ydeevne, især når flere processer kører samtidigt.

## Usage
Den grundlæggende syntaks for `nice`-kommandoen er som følger:

```bash
nice [options] [command]
```

## Common Options
- `-n, --adjustment=N`: Angiver justeringen af prioritet. Standardværdien er 10, og værdier kan være negative (hvis du har de nødvendige rettigheder) eller positive.
- `-h, --help`: Viser hjælp og information om brugen af `nice`.
- `-V, --version`: Viser versionsinformation for `nice`.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du kan bruge `nice`:

1. Kør et program med standardprioritet:
   ```bash
   nice ./my_program
   ```

2. Kør et program med en lavere prioritet (mere venlig):
   ```bash
   nice -n 10 ./my_program
   ```

3. Kør et program med en højere prioritet (mindre venlig):
   ```bash
   sudo nice -n -5 ./my_program
   ```

4. Tjek den nuværende prioritet af en kørende proces:
   ```bash
   ps -o pid,ni,cmd
   ```

## Tips
- Brug `nice` i kombination med `nohup` for at køre langvarige processer, der ikke stopper, når du logger ud.
- Vær opmærksom på, at kun brugere med de rette rettigheder kan sænke prioriteten af en proces til en negativ værdi.
- Overvåg systemets ydeevne, når du justerer prioriteten af processer, for at finde den bedste balance mellem ressourcer.