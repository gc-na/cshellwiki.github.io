# [Linux] Bash write brug: Send beskeder til brugere

## Oversigt
`write`-kommandoen bruges til at sende beskeder til andre brugere, der er logget ind på systemet. Det er en nyttig måde at kommunikere direkte med en anden bruger i realtid.

## Brug
Den grundlæggende syntaks for `write`-kommandoen er som følger:

```bash
write [bruger] [terminal]
```

Her er `[bruger]` navnet på den bruger, du vil sende en besked til, og `[terminal]` er den specifikke terminal, hvis det er nødvendigt.

## Almindelige muligheder
- `-n`: Angiv ikke terminalen, hvis brugeren har flere terminaler åbne.
- `-h`: Vis hjælp og afslut.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `write`-kommandoen:

1. Send en besked til en bruger ved navn "peter":
   ```bash
   write peter
   ```
   (Skriv din besked og tryk på `Ctrl+D` for at sende.)

2. Send en besked til en specifik terminal af brugeren "anna":
   ```bash
   write anna pts/1
   ```
   (Skriv din besked og afslut med `Ctrl+D`.)

3. Send en besked til en bruger uden at angive terminal:
   ```bash
   write peter
   ```
   (Skriv din besked og tryk på `Ctrl+D` for at afslutte.)

## Tips
- Sørg for, at den bruger, du sender beskeden til, er logget ind og har en åben terminal.
- Brug `mesg n` for at forhindre andre i at sende beskeder til dig, hvis du ikke ønsker at modtage dem.
- Vær opmærksom på, at `write`-beskeder kan være synlige for alle, der har adgang til den terminal, så vær forsigtig med følsomme oplysninger.